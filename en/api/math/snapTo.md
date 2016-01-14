# [qc.Math](README.md).snapTo

## Prototype
* number snapTo(input, gap, start)

## Paramters
| Paramter | Type | Description |
| ------------- | ------------- | -------------|
| input | number | The value to snap.   |
| gap | number | The interval gap of the grid.  |
| start | number | Optional starting offset for gap.        |
| return | number |  |

## Description
Snap a value to nearest grid slice, using rounding.

## Example
````
    // return 10
    var ret = game.math.snapTo(12, 5, 0);

    // return 15
    var ret = game.math.snapTo(13, 5, 0);
````
