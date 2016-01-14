# [qc.Math](README.md).clamp

## Prototype
* number clamp(x, min, max)

## Paramters
| Paramter | Type | Description |
| ------------- | ------------- | -------------|
| x | number |  |
| min | number |  |
| max | number |  |
| return | number |  |

## Description
Force a value within the boundaries by clamping `x` to the range `[a, b]`.

## Example
````
    // return 3
    var ret = game.math.clamp(3, 2, 4);

    // return 2
    var ret = game.math.clamp(1, 2, 4);

    // return 4
    var ret = game.math.clamp(5, 2, 4);
````
