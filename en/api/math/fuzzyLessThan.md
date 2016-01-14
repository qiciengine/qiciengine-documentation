# [qc.Math](README.md).fuzzyLessThan

## Prototype
* boolean fuzzyLessThan(a, b, epsilon)

## Paramters
| Paramter | Type | Description |
| ------------- | ------------- | -------------|
| a | number | value |
| b | number | value |
| epsilon | number | small value |
| return | boolean | True if a<b+epsilon |

## Description
`a` is fuzzyLessThan `b` if it is less than b + epsilon.

## Example
````
    // return true
    var ret = game.math.fuzzyLessThan(1.22, 1.23, 0.00001);
````
