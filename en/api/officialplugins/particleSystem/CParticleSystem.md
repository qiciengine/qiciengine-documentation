# qc.ParticleSystem
inherit [qc.Node](../../gameobject/CNode.md)

## Description
A Particle System simulates fluid entites such as liquids, clouds and flames by generating and animating large numbers of small images in the scene. Inherit from [Node](../../gameobject/CNode.md).

## Variables
| Variable Name | Type | Description |
| ------------- |-------------| -------------|
| texture | qc.Texture | The texture that particles will use.  |
| zoneType | number | The shape of the emission zone. Currently supports four types: Zone.POINT(point), Zone.LINE(line), Zone.CIRCLE(circle) and Zone.RECTANGLE(rectangle)  |
| edgeEmission | bool | Whether the particles will be emitted from the edge of the zone. |
| zoneLength | number | The length of emission zone. Only takes effect when zoneType is Zone.LINE. |
| zoneRotation | number | The rotation of emission zone. Only takes effect when zoneType is Zone.LINE. |
| zoneRadius | number | The radius of emission zone. Only takes effect when zoneType is Zone.CIRCLE. |
| zoneWidth | number | The width of emission zone. Only takes effect when zoneType is Zone.RECTANGLE. |
| zoneHeight | number | The height of emission zone. Only takes effect when zoneType is Zone.RECTANGLE.  |
| frequency | number |  How often per emission, in seconds. |
| quantity | number | How many particles will be generated per emission. |
| repeat | number | The repeat count of emission, -1 means loop always. |
| delay | number | The delay time of the first emission in seconds. |
| lifespan | Array | How long each particle lives once it is emitted in seconds. |
| angle | Array | The emission angle of particles, the value is picked at random within specified min-max range. |
| blendMode | number | The blend mode of particle. |
| startColor | qc.Color | The start color of particle. |
| startColorVariation | number | The variation of start color. |
| endColor | qc.Color | The target color of particle. |
| endColorVariation | number | The variation of end color. |
| startAlpha | Array | The transparency of particles, the value is picked at random within specified min-max range. |
| startScale | Array |  The start scale of particles, the value is picked at random within specified min-max range. |
| startRotation | Array | The start rotation of particles, the value is picked at random within specified min-max range. |
| startVelocity | Array | The start velocity of particles, the value is picked at random within specified min-max range. |
| angularVelocity | Array | The start angular velocity of particles, the value is picked at random within specified min-max range. |
| gravity | qc.Point | The gravity of particle systems. |
| maxParticles | number | The maximum number of particles, the emission will be stopped when the number of particles exceeds this value. |
| playOnAwake | boolean | Whether the particle system will start playing automatically. |
| initialFrame | Array | The initial frame of a particle when play sprite sheet animation, the value is picked at random within specified min-max range. |
| frameRate | Array | The frame rate of animation, the value is picked at random within specified min-max range. |
| enableColorCurve | boolean | Whether enable a curve to control the color of particles. |
| colorCurve | qc.BezierCurve | Curve to control the color of particles, the color will vary linearly between start color and target color if the curve is disabled. |
| enableAlphaCurve | boolean | Whether enable a curve to control the transparency of particles. |
| alphaCurve | qc.BezierCurve | Curve to control the transparency of each particle duration its lifespan.. |
| enableScaleCurve | boolean | Whether enable a curve to control the scale of particles. |
| scaleCurve | qc.BezierCurve | Curve to control the scale of each particle duration its lifespan. |
| enableVelocityCurve | boolean | Whether enable a curve to control the velocity of particles. |
| velocityCurve | qc.BezierCurve | Curve to control the velocity of each particle duration its lifespan. |
| enableAngularVelocityCurve | boolean | Whether enable a curve to control the angular velocity of particles. |
| angularVelocityCurve | qc.BezierCurve | Curve to control the angular velocity of each particle duration its lifespan. |

## Methods
| Method | Description |
| ------------- |-------------|
| [start](methods/start.md) | Start playing the particle system. |
| [pause](methods/pause.md) | Pause playing the particle system. |
| [clear](methods/clear.md) | Clear all emitted particles. |
| [reset](methods/reset.md) | Reset the particle system. |

## Manual
[ParticleSystem](http://docs.qiciengine.com/manual/Plugin/ParticleSystem/ParticleSystem.html)
