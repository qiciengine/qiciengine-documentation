# [qc.Math](README.md).minSub

## Prototype
* number minSub(value, amount, min)

## Paramters
| Paramter | Type | Description |
| ------------- | ------------- | -------------|
| value | number | The base value.       |
| amount | number | The amount to subtract from the base value.    |
| min | number | The minimum the value is allowed to be.    |
| return | number |  The new value. |

## Description
 Subtracts the given amount from the value, but never let the value go below the specified minimum.

## Example
````
    // return 2
    var ret = game.math.minSub(3, 1, 1);

    // return 4
    var ret = game.math.minSub(3, 1, 4);
````
