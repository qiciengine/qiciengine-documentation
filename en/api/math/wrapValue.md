# [qc.Math](README.md).wrapValue

## Prototype
* number wrapValue(value, amount, max)

## Paramters
| Paramter | Type | Description |
| ------------- | ------------- | -------------|
| value | number |  The value to add the amount to.  |
| amount | number | The amount to add to the value. |
| max | number | The maximum the value is allowed to be.  |
| return | number |  The wrapped value.        |

## Description
Adds value to amount and ensures that the result always stays between 0 and max, by wrapping the value around.
````
        var diff;
        value = Math.abs(value);
        amount = Math.abs(amount);
        max = Math.abs(max);
        diff = (value + amount) % max;

        return diff;
````

## Example
````
    // return 8
    var ret = game.math.wrapValue(3, 5, 10);

    // return 0
    var ret = game.math.wrapValue(5, 5, 10);

    // return 1
    var ret = game.math.wrapValue(6, 5, 10);
````
