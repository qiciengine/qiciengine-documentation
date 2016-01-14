# [qc.Emitter](CEmitter.md).setScale

## Prototype
* void setScale(min:number, max:number, rate:number, ease:function, yoyo:boolean)

## Parameters
| Parameter | Type | Description |
| ------------- | ------------- | -------------|
| min | number | The minimum value of Particle.scale. |
| max | number | The maximum value of Particle.scale |
| rate | number | The rate (in ms) at which the particles will change in scale from min to max, or set to zero to pick a random size between the two. |
| ease | function | If you've set a rate > 0 this is the easing formula applied between the min and max values. |
| yoyo | boolean | If you've set a rate > 0 you can set if the ease will yoyo or not (i.e. ease back to its original values) |

## Description
A more compact way of setting the scale constraints of the particles.  
The rate parameter, if set to a value above zero, lets you set the speed and ease which the Particle uses to change in scale from min to max across both axis.  
If rate is zero, which is the default, the particle won't change scale during update, instead it will pick a random scale between min and max on emit.