# [qc.Math](README.md).snapToCeil

## Prototype
* number snapToCeil(input, gap, start)

## Paramters
| Paramter | Type | Description |
| ------------- | ------------- | -------------|
| input | number | The value to snap.          |
| gap | number | The interval gap of the grid.          |
| start | number | Optional starting offset for gap.  |
| return | number |  |

## Description
Snap a value to nearest grid slice, using ceil.

## Example
````
    // return 15
    var ret = game.math.snapToCeil(11, 5, 0);

    // return 15
    var ret = game.math.snapToCeil(14, 5, 0);
````
