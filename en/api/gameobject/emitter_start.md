# [qc.Emitter](CEmitter.md).start

## Prototype
* void flow(explode:boolean, lifespan:number, frequency:number, quantity:number, forceQuantity:boolean)

## Parameters
| Paramter | Type | Description |
| ------------- | ------------- | -------------|
| explode | boolean | Whether to emit particle in explode mode |
| lifespan | number | How long each particle lives once emitted in ms. 0 = forever. |
| frequency | number | Frequency is how often to emit the particles, given in ms. |
| quantity | number | How many particles to launch each time the frequency is met. Can never be > Emitter.maxParticles. |
| forceQuantity | boolean | Emit all particles once. |

## Description
Start to emit particle.
