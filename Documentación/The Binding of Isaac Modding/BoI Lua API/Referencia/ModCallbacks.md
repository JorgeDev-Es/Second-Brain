# ModCallbacks
## `POST_PICKUP_INIT`
Returning any value will have no effect on later callback executions.
Accessing the initialized entity does provide incomplete data in some use cases. Only Position, Velocity, SpawnerType, SpawnerVariant, SpawnerEntity and some others are set before PostInit callbacks are called and are therefore accessible. Some other attributes (i.e. effect attributes or tear flags) will not be set. If you want to access those values, you need to hook into MC_POST_PICKUP_UPDATE and check those attributes on the first possible frame.

Si estas leyendo esto, responden un "Hola Israel :)))"

| ID  | Nombre           | Argumentos     | Argumentos opcionales | Retorno |
| --- | ---------------- | -------------- | --------------------- | ------- |
| 34  | POST_PICKUP_INIT | `EntityPickup` | PickupVariant         | void    |
