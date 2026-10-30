# Estructuras Clave del Motor (`uking` / `KingSystem` / `sead`)

Referencia rápida de la arquitectura de clases y estructuras principales de *Breath of the Wild* (Switch 1.5.0) para identificar punteros `this`, herencia y miembros al decompilar.

---

## 1. Primitivas de `sead`

- **Strings:**
  - `sead::SafeStringBase<char>` (`SafeString`): contiene `vptr` (offset `0x0`) y `const char* mStringTop` (offset `0x8`).
  - `sead::BufferedSafeStringBase<char>`: hereda de `SafeString`, añade `s32 mBufferSize` (offset `0x10`).
  - `sead::FixedSafeString<N>`: hereda de `BufferedSafeStringBase<char>`, añade `char mBuffer[N]` en línea.
- **Contenedores:**
  - `sead::Buffer<T>`: contiene `s32 mSize` (offset `0x0`) y `T* mBuffer` (offset `0x8`).
  - `sead::PtrArrayImpl`: contiene `s32 mPtrNum` (`0x0`), `s32 mPtrNumMax` (`0x4`) y `void** mPtrs` (`0x8`).
  - `sead::ListImpl`: contiene `ListNode mStartEnd` (`0x0`, `mPrev` y `mNext`) y `s32 mCount` (`0x10`).
  - `sead::OffsetList<T>`: hereda de `ListImpl`, añade `s32 mOffset` (`0x14`).
- **Gestión de Memoria y Sincronización:**
  - `sead::IDisposer`: `vptr` (`0x0`), `Heap* mDisposerHeap` (`0x8`), `ListNode mListNode` (`0x10`). Tamaño total: `0x20`.
  - `sead::CriticalSection`: hereda de `IDisposer`, envuelve `nn::os::MutexType mCriticalSectionInner` (`0x20`).

---

## 2. Procesos Base y Actores (`ksys::act`)

### `ksys::act::BaseProc`
Clase base de todos los objetos procesables del juego:
- `vptr` (`0x0`)
- `sead::FixedSafeString<64> mName` (`0x8`)
- `u32 mId` (`0x60`)
- `State mState` (`Init = 0`, `Calc = 1`, `Sleep = 2`, `Delete = 3`)
- `u8 mPriority`, `u8 mCreatePriorityState`, `u8 mCounter`
- `BaseProcLinkData* mBaseProcLinkData`
- `sead::BitFlag16 mSkippedJobTypesMask`, `mSpecialJobTypesMask`
- `sead::TypedBitFlag<Flags, sead::Atomic<u32>> mFlags`
- `sead::TypedBitFlag<StateFlags, sead::Atomic<u32>> mStateFlags`
- Punteros a nodos padre/hijo de cálculo (`mConnectedCalcParent`, `mConnectedCalcChild`)
- `sead::SafeArray<BaseProcJobHandler*, 7> mJobHandlers`
- `BaseProcMapNode mMapNode`, `BaseProcUnit* mProcUnit`, `sead::Atomic<s32> mRefCount`

### `ksys::act::Actor`
Hereda de `ksys::act::BaseProc` y `ksys::MessageTransceiverRxOnly::IHandler`:
- Cuerpos rígidos atómicos: `mMainBody`, `mTgtBody` (`sead::Atomic<phys::RigidBody*>`)
- Handlers de trabajo: `mJob0`, `mJob1`, `mJob2`, `mJob4`
- Nodos de listas intrusivas: `mActiveActorListNode`, `mActorsThatLostPlacementObjListNode`, `mVillagerListNode`
- Transformaciones y movimiento: `sead::Matrix34f mMtx`, `mPhysicsMtx`, `mHomeMtx`, `sead::Vector3f mVelocity`, `mAngVelocity`, `mScale`
- Distancias de LOD/spawning: `mDispDistanceSq`, `mDeleteDistanceSq`, `mLoadDistance`
- Componentes principales del Actor:
  - `gsys::Model* mModel`
  - `sead::BoundBox3f mAabb`
  - `Awareness* mAwareness`
  - `ai::RootAi* mRootAi`
  - `as::ASList* mASList`
  - `xlink2::XLink* mXLink`
  - `ActorParam* mActorParam`
  - `phys::InstanceSet* mPhysics`
  - `BoneControl* mBoneControl`
  - `phys::StaticCompoundRigidBodyGroup* mFieldBodyGroup`
  - `sead::Heap* mDualHeap`, `mDualHeap2`, `mHeap`
  - `Attention* mAttention`
  - `ActorMessageTransceiver mMsgTransceiver`
  - `u32 mHashId`, `map::MubinIter mMapObjIter`
  - `Chemical* mChemical`, `Reaction* mReaction`
  - `mii::UMii* mUMii`

---

## 3. Inteligencia Artificial (`ksys::act::ai`)

El sistema de IA de cada `Actor` se gestiona desde `RootAi` y se divide en 4 clases base que heredan o usan `ActionBase`:
- `ActionBase`: contiene `vptr`, `Actor* mActor`, `ParamPack mParams`, `s16 mDefinitionIdx`, `s8 mRootIdx`, `mFlags`.
- `Ai`: hereda de `ActionBase`. Añade índices de hijos (`mChildIdx`, `mPrevChildIdx`, `mPendingChildIdx`, `mNewChildIdx`) y `sead::Buffer<ActionBase*> mChildren`.
- `Action`: hereda de `ActionBase`. Representa una acción concreta en hoja.
- `Behavior`: contiene `vptr`, `Actor* mActor`, `u16 mDefIdx`. Se ejecuta pasivamente en cada frame según su prioridad.
- `Query`: contiene `vptr`, `Actor* mActor`, `ParamPack mParamPack`, `s32 mDefIdx`. Evalúa condiciones booleanas o enteras para árboles de decisión y EventFlow.

Convención de sufijos en punteros de parámetros de IA/Acciones:
- `_s`: Parámetro estático (*static param*, leído del archivo `.baiprog`).
- `_d`: Parámetro dinámico (*dynamic param*, pasado desde el padre o EventFlow).
- `_m`: Parámetro de unidad de mapa (*map unit param*, leído del `.ymap` / `MubinIter`).
- `_a`: Enlace de datos de IA (*AI data / AITree variable*, compartido entre nodos de IA).

---

## 4. Sistema de Guardado (`ksys::gdt`)

- `ksys::gdt::GameData`: hereda de `sead::DirectResource`. Contiene `sead::Buffer<Flag<T>>` para los 9 tipos de flags simples (`bool`, `s32`, `f32`, `FixedSafeString<32/64/256>`, `Vector2f/3f/4f`) y `sead::PtrArray<sead::Buffer<Flag<T>>>` para sus equivalentes en arreglos (`ArrayFlags`).
- `ksys::gdt::Flag<T>`: hereda de `FlagT<T>`, almacena `mType`, `FlagProperties mProperties`, `ConfigType mConfig` (con `initial_value`, `min`, `max`), `RawValueType mValue`, `u32 mHash` y `FlagDebugData* mDebugData`.

---

## 5. Sistema de Recursos y Parámetros (`ksys::res` y `agl::utl`)

- `agl::utl::IParameterObj` / `ParameterObj`: lista enlazada de parámetros (`ParameterBase* mParamListHead`, `mParamListTail`, `mNameHash`).
- `agl::utl::Parameter<T>`: hereda de `ParameterBase` (`vptr`, `u32 mNameHash`, `ParameterBase* mNext`) y guarda `T mValue`.
- `ksys::res::ParamIO`: hereda de `agl::utl::IParameterIO` y `sead::hostio::Node`. Base de recursos `.bxml`, `.bgparamlist`, `.bdmgparam`, `.bphysics`, `.baiprog`, `.bdrop`, `.bshop`, `.brecipe`, `.blod` y `.bumii`.
