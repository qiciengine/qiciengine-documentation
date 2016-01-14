# [qc.Math](README.md).linear

## Prototype
* number linear(p0, p1, t)

## Paramters
| Paramter | Type | Description |
| ------------- | ------------- | -------------|
| p0 | number | Start value |
| p1 | number | End value |
| t | number | The percentage of interpolation, between 0 and 1.       |
| return | number | The interpolated value         |

## Description
Calculates a linear (interpolation) value over t.

## Example
````
    // return 2.8
    var ret = game.math.linear(1,10,0.2);
````
