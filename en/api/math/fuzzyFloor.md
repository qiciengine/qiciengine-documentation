# [qc.Math](README.md).fuzzyFloor

## Prototype
* number fuzzyFloor(val, epsilon)

## Paramters
| Paramter | Type | Description |
| ------------- | ------------- | -------------|
| val | number | value |
| epsilon | number | small value |
| return | number |  floor(val-epsilon)   |

## Description
 floor(val-epsilon)

## Example
````
    // return 2
    var ret = game.math.fuzzyFloor(1.99999999, 0.00001);

    // return 1
    var ret = game.math.fuzzyFloor(1.9888888, 0.00001);
````
