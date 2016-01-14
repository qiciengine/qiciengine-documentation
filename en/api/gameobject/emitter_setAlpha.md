# [qc.Emitter](CEmitter.md).setAlpha

## Prototype
* void setAlpha(min:number, max:number, rate:number, ease:function, yoyo:boolean)

## Parameters
| Paramter | Type | Description |
| ------------- | ------------- | -------------|
| min | number | The minimum value for this range. |
| max | number | The maximum value for this range. |
| rate | number | The rate (in ms) at which the particles will change in alpha from min to max, or set to zero to pick a random alpha between the two. |
| ease | function | If you've set a rate > 0 this is the easing formula applied between the min and max values. |
| yoyo | boolean | If you've set a rate > 0 you can set if the ease will yoyo or not (i.e. ease back to its original values) |

## Description
A more compact way of setting the alpha constraints of the particles.  
The rate parameter, if set to a value above zero, lets you set the speed at which the Particle change in alpha from min to max.  
If rate is zero, which is the default, the particle won't change alpha - instead it will pick a random alpha between min and max on emit.