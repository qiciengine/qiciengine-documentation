# [qc.Math](README.md).ceilTo

## Prototype
* number ceilTo(value, place, base)

## Paramters
| Paramter | Type | Description |
| ------------- | ------------- | -------------|
| value | number | The value to ceil. |
| place | number | The place to ceil to.  |
| base | number | The base to ceil in... default is 10 for decimal. |
| return | number |  |

## Description
Ceil to some places comparative to a `base`, default is 10 for decimal place.
The `place` is represented by the power applied to `base` to get that place.

## Example
````
    // return 300
    var ret = game.math.ceilTo(285.7142, 2);

    // return 290
    var ret = game.math.ceilTo(285.7142, 1);

    // return 286
    var ret = game.math.ceilTo(285.7142, 0);

    // return 285.8
    var ret = game.math.ceilTo(285.7162, -1);

    // return 285.72
    var ret = game.math.ceilTo(285.7162, -2);
````
