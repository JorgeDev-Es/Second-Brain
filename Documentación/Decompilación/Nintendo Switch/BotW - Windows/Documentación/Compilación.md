# Compilación
## 
```PowerShell
cmake -S . -B build -G Ninja -DCMAKE_BUILD_TYPE=RelWithDebInfo -DCMAKE_TOOLCHAIN_FILE=toolchain/ToolchainNX64 -DUKING_LINKER=D:/botw-decomp-windows/toolchain/clang-4.0.1/bin/ld.lld.exe -DCMAKE_CXX_COMPILER_LAUNCHER=ccache

```

```PowerShell
ninja -C build
```