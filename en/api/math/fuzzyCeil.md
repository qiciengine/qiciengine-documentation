# [qc.Math](README.md).fuzzyCeil

## Prototype
* number fuzzyCeil(val, epsilon)

## Paramters
| Paramter | Type | Description |
| ------------- | ------------- | -------------|
| val | number | value |
| epsilon | number | small value |
| return | number | ceiling(val-epsilon)     |

## Description
ceiling(val-epsilon)

## Example
````
    // return 2
    var ret = game.math.fuzzyCeil(1.0001, 0.00001);

    // return 1
    var ret = game.math.fuzzyCeil(1.00000001, 0.00001);
````
