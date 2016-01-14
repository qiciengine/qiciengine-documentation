# [qc.Math](README.md).sign

## Prototype
* number sign(value)

## Paramters
| Paramter | Type | Description |
| ------------- | ------------- | -------------|
| value | number | value |
| return | number | An integer in {-1, 0, 1}    |

## Description
A value representing the sign of the value: -1 for negative, +1 for positive, 0 if value is 0.

## Example
````
    // return 1
    var ret = game.math.sign(4);

    // return 0
    var ret = game.math.sign(0);

    // return -1
    var ret = game.math.sign(-4);
````
