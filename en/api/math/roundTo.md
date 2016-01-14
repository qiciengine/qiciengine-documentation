# [qc.Math](README.md).roundTo

## Prototype
* number roundTo(value, place, base)

## Paramters
| Paramter | Type | Description |
| ------------- | ------------- | -------------|
| value | number | The value to round.   |
| place | number | The place to round to.  |
| base | number |The base to round in... default is 10 for decimal.   |
| return | number |  |

## Description
Round to some place comparative to a `base`, default is 10 for decimal place.
The `place` is represented by the power applied to `base` to get that place.

## Example
````
    // return 300
    var ret = game.math.roundTo(285.7142, 2);

    // return 290
    var ret = game.math.roundTo(285.7142, 1);

    // return 286
    var ret = game.math.roundTo(285.7142, 0);

    // return 285.7
    var ret = game.math.roundTo(285.7162, -1);

    // return 285.72
    var ret = game.math.roundTo(285.7162, -2);
````
