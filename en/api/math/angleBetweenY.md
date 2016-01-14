# [qc.Math](README.md).angleBetweenY

## Prototype
* number angleBetweenY(x1, y1, x2, y2)

## Paramters
| Paramter | Type | Description |
| ------------- | ------------- | -------------|
| x1 | number |  |
| y1 | number |  |
| x2 | number |  |
| y2 | number | |
| return | number |  The angle, in radians.      |

## Description
Find the angle of a segment from (x1, y1) -> (x2, y2).
Note that the difference between this method and Math.angleBetween is that this assumes the y coordinate travels down the screen.

## Example
````
    // return -0.4636476090008061
    var ret = game.math.angleBetweenY(1, 2, 0, 4);
````
