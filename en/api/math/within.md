# [qc.Math](README.md).within

## Prototype
* boolean within(a, b, tolerance)

## Paramters
| Paramter | Type | Description |
| ------------- | ------------- | -------------|
| a | number | The first number to check      |
| b | number |  The second number to check |
| tolerance | number | The tolerance. Anything equal to or less than this is considered within the range.     |
| return | boolean | True if a is <= tolerance of b.  |

## Description
Checks if two values are within the given tolerance of each other.
````
    return (Math.abs(a - b) <= tolerance);
````

## Example
````
    // return true
    var ret = game.math.within(3, 2, 2);
````
