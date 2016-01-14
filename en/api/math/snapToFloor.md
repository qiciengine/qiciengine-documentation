# [qc.Math](README.md).snapToFloor

## Prototype
* number snapToFloor(input, gap, start)

## Paramters
| Paramter | Type | Description |
| ------------- | ------------- | -------------|
| input | number | The value to snap.  |
| gap | number | The interval gap of the grid. |
| start | number | Optional starting offset for gap.   |
| return | number |  |

## Description
Snap a value to nearest grid slice, using floor.

## Example
````
    // return 10
    var ret = game.math.snapToFloor(11, 5, 0);

    // return 10
    var ret = game.math.snapToFloor(14, 5, 0);
````
