# [qc.Math](README.md).getRandom

## Prototype
* number getRandom(objects, startIndex, length)

## Paramters
| Paramter | Type | Description |
| ------------- | ------------- | -------------|
| objects | array | An array of objects.   |
| startIndex | number | Optional offset off the front of the array. Default value is 0, or the beginning of the array.   |
| length | length | Optional restriction on the number of values you want to randomly select from.  |
| return | number | The random object that was selected.    |

## Description
Fetch a random entry from the given array.
 Will return null if there are no array items that fall within the specified range or if there is no item for the randomly choosen index.

## Example
````
    // return 3
    var ret = game.math.getRandom([3,4,2,5,9]);

    // return 5
    var ret = game.math.getRandom([3,4,2,5,9]);
````
