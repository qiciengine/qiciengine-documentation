# [qc.Math](README.md).floorTo

## Prototype
* number floorTo(value, place, base)

## Paramters
| Paramter | Type | Description |
| ------------- | ------------- | -------------|
| value | number | The value to floor.  |
| place | number | The place to floor to. |
| base | number | The base to floor in... default is 10 for decimal. |
| return | number |  |

## Description
Floor to some place comparative to a `base`, default is 10 for decimal place.
The `place` is represented by the power applied to `base` to get that place.

## Example
````
    // return 200
    var ret = game.math.roundTo(285.7142, 2);

    // return 280
    var ret = game.math.roundTo(285.7142, 1);

    // return 285
    var ret = game.math.roundTo(285.7142, 0);

    / return 285.7
    var ret = game.math.roundTo(285.7162, -1);

    / return 285.71
    var ret = game.math.roundTo(285.7162, -2);
````
