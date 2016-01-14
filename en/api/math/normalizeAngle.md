# [qc.Math](README.md).normalizeAngle

## Prototype
* number normalizeAngle(angleRad)

## Paramters
| Paramter | Type | Description |
| ------------- | ------------- | -------------|
| angleRad | number | The angle to normalize, in radians.  |
| return | number | Returns the angle, fit within the [0,2pi] range, in radians.     |

## Description
Normalizes an angle to the [0,2pi) range.

## Example
````
    // return Math.PI
    var ret = game.math.normalizeAngle(3 * Math.PI);
````
