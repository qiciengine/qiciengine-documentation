# [qc.Math](README.md).min

## Prototype
* number min(n1,n2,...)
* number min([n1,n2,...])

## Paramters
| Paramter | Type | Description |
| ------------- | ------------- | -------------|
| n1... | number | many value |
| [n1,n2,...] | array | An array of value |
| return | number |  The lowest value from those given.   |

## Description
Variation of Math.min that can be passed either an array of numbers or the numbers as parameters.

## Example
````
    // return -5
    var ret = game.math.min(1,2,-5,4);

    // return -5
    var ret = game.math.min([1,2,-5,4]);
````
