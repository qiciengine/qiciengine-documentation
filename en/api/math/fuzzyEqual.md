# [qc.Math](README.md).fuzzyEqual

## Prototype
* boolean fuzzyEqual(a, b, epsilon)

## Paramters
| Paramter | Type | Description |
| ------------- | ------------- | -------------|
| a | number | value |
| b | number | value |
| epsilon | number | small value |
| return | boolean | True if abs(a-b)<epsilon  |

## Description
Two number are fuzzyEqual if their difference is less than epsilon.

## Example
````
    // return true
    var ret = game.math.fuzzyEqual(1.23, 1.23, 0.00001);
````
