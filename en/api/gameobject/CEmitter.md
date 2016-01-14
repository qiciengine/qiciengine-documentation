# qc.Emitter

## Description
Emitter is a lightweight particle emitter.
It can be used for one-time explosions or for continuous effects like rain and fire.
All it really does is launch Particle objects out at set intervals, and fixes their positions and velocities accordingly.

## Variables
| Variable Name         |   Type      |  Description        |
| ------------- |-------------|-------------|
| maxParticles | int | Default 50. The total number of particles in this emitter. |
| texture | [qc.Atlas](../assets/Atlas.md) | The texture atlas that the particle will use. |
| frames | Array | Array of frames that the particle will use. Frame is picked at random. |
| bounce | qc.Point | How much each particle should bounce on each axis. 1 = full bounce, 0 = no bounce. |
| area | qc.Rectangle | The area of the emitter. Particles can be randomly generated from anywhere within this rectangle. |
| minParticleSpeed | qc.Point | The minimum possible velocity of a particle. |
| maxParticleSpeed | qc.Point | The maximum possible velocity of a particle. |
| scaleFrom | qc.Point | 粒子的起始缩放比例。
| scaleTo | qc.Point | 粒子的终止缩放比例 |
| scaleDuration | number | 缩放持续的时间，单位毫秒 |
| scaleEase | string | 缩放变化的曲线 |
| scaleYoyo | boolean | 是否来回缩放 |
| scaleData | Array | 发射时按照数组顺序赋予缩放值 |
| minRotation | number | 粒子最小的旋转角度 |
| maxRotation | number | 粒子最大的旋转角度 |
| alphaFrom | number | 粒子起始透明度 |
| alphaTo | number | 粒子终止的透明度 |
| alphaDuration | number | 透明度变化的持续时间 |
| alphaEase | string | 透明度变化的曲线 |
| alphaYoyo | boolean | 是否来回变化透明度 |
| alphaData | Array | 发射时按数组顺序赋予透明度 |
| gravity | number | The particle's gravity  |
| particleDrag | qc.Point | The X and Y drag component of particles launched from the emitter. |
| angularDrag | qc.Point | The angular drag component of particles launched from the emitter if they are rotating. |
| frequency | number | How often a particle is emitted in ms. |
| lifespan | number | How long each particle lives once it is emitted in ms. Default is 2 seconds. Set lifespan to 'zero' for particles to live forever. |
| on | boolean | Determines whether the emitter is currently emitting particles. It is totally safe to directly toggle this. |
| emitX | number | The point the particles are emitted from. |
| emitY | number | The point the particles are emitted from. |
| collide | boolean | If you want the particles to be able to collide with other Arcade Physics bodies then set this to true. |
| collideWorldBounds | boolean | A particle can be set to collide against the World bounds automatically and rebound back into the World if this is set to true. Otherwise it will leave the World. |
| particleBringToTop | boolean | If this is `true` then when the Particle is emitted it will be bought to the top of the Emitters display list. |
| paritcleSendToBack | boolean | If this is `true` then when the Particle is emitted it will be sent to the back of the Emitters display list. |

## Methods
| Method | Description |
| ------------- |-------------|
| [kill](emitter_kill.md) | Turn off all the particles and the emitter. |
| [revive](emitter_revive.md) | Handy for bringing game objects "back to life". Just sets alive and exists back to true. |
| [explode](emitter_explode.md) | Call this function to emit the given quantity of particles at all once (an explosion) |
| [flow](emitter_flow.md) | Call this function to start emitting a flow of particles at the given frequency. |
| [start](emitter_start.md) | Start to emit particle |
| [setAlpha](emitter_setAlpha.md) | A more compact way of setting the alpha constraints of the particles. |
| [setScale](emitter_setScale.md) | A more compact way of setting the scale constraints of the particles. |
| [rebuild](emitter_rebuild.md) | After all paramters are set up, call this function to start emitting. |

## Demo
[Partical Demo](http://engine.qiciengine.com/demo/index.html#anchor_Particle)