# [qc.Math](README.md).wrap

## Prototype
* number wrap(value, min, max)

## Paramters
| Paramter | Type | Description |
| ------------- | ------------- | -------------|
| value | number | The value to wrap.    |
| min | number | The minimum the value is allowed to be.  |
| max | number | The maximum the value is allowed to be, should be larger than `min`. |
| return | number | The wrapped value. |

## Description
 Ensures that the value always stays between min and max, by wrapping the value around.
 If `max` is not larger than `min` the result is 0.
````
    var range = max - min;
    var result = (value - min) % range;
    if (result < 0)
    {
        result += range;
    }

    return result + min;
````

## Example
````
    // return 8
    var ret = game.math.wrap(3, 5, 10);

    // return 9
    var ret = game.math.wrap(4, 5, 10);

    // return 9
    var ret = game.math.wrap(9, 5, 10);

    // return 6
    var ret = game.math.wrap(11, 5, 10);

    // return 7
    var ret = game.math.wrap(12, 5, 10);
````
