# [qc.Math](README.md).maxAdd

## Prototype
* number maxAdd(value, amount, max)

## Paramters
| Paramter | Type | Description |
| ------------- | ------------- | -------------|
| value | number | The value to add the amount to.    |
| amount | number | The amount to add to the value.       |
| max | number | The maximum the value is allowed to be.    |
| return | number |  |

## Description
Adds the given amount to the value, but never let the value go over the specified maximum.

## Example
````
    // return 2
    var ret = game.math.maxAdd(1, 3, 2);

    // return 4
    var ret = game.math.maxAdd(1, 3, 4);
````
