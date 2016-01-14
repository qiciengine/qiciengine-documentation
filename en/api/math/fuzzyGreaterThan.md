# [qc.Math](README.md).fuzzyGreaterThan

## Prototype
* boolean fuzzyGreaterThan(a, b, epsilon)

## Paramters
| Paramter | Type | Description |
| ------------- | ------------- | -------------|
| a | number | value |
| b | number | value |
| epsilon | number | small value |
| return | boolean |  True if a>b+epsilon    |

## Description
 `a` is fuzzyGreaterThan `b` if it is more than b - epsilon.

## Example
````
    // return true
    var ret = game.math.fuzzyGreaterThan(1.232, 1.23, 0.00001);
````
