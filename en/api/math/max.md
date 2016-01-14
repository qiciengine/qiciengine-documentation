# [qc.Math](README.md).max

## Prototype
* number max(n1,n2,...)
* number max([n1,n2,...])

## Paramters
| Paramter | Type | Description |
| ------------- | ------------- | -------------|
| n1... | number |  many value |
| [n1,n2,...] | array | An array of value |
| return | number | The largest value from those given.     |

## Description
Variation of Math.max that can be passed either an array of numbers or the numbers as parameters.

## Example
````
    // return 4
    var ret = game.math.max(1,2,-5,4);

    // return 4
    var ret = game.math.max([1,2,-5,4]);
````
