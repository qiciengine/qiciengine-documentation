# [qc.Emitter](CEmitter.md).flow

## Prototype
* void flow(lifespan:number, frequency:number, quantity:number, total:number, immediate:boolean)

## Parameters
| Parameter | Type | Description |
| ------------- | ------------- | -------------|
| lifespan | number | How long each particle lives once emitted in ms. 0 = forever. |
| frequency | number | Frequency is how often to emit the particles, given in ms. |
| quantity | number | How many particles to launch each time the frequency is met. Can never be > Emitter.maxParticles. |
| total | number | How many particles to launch in total. If -1 it will carry on indefinitely. |
| immediate | boolean | Should the flow start immediately (true) or wait until the first frequency event? (false) |

## Description
Call this function to start emitting a flow of particles at the given frequency.  
It will carry on going until the total given is reached.  
Each time the flow is run the quantity number of particles will be emitted together.  
If you set the total to be 20 and quantity to be 5 then flow will emit 4 times in total (4 x 5 = 20 total)  
If you set the total to be -1 then no quantity cap is used and it will keep emitting.