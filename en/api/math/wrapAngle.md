# [qc.Math](README.md).wrapAngle

## Prototype
* number wrapValue(angle, radians)

## Paramters
| Paramter | Type | Description |
| ------------- | ------------- | -------------|
| angle | number | The angle value to wrap   |
| radians | boolean |  Set to `true` if the angle is given in radians, otherwise degrees is expected.  |
| return | number |  The new angle value; will be the same as the input angle if it was within bounds.  |

## Description
Keeps an angle value between -180 and +180; or -PI and PI if radians.
````
        return radians ? this.wrap(angle, -Math.PI, Math.PI) : this.wrap(angle, -180, 180);
````

## Example
````
    // return -10
    var ret = game.math.wrapAngle(350);
````
