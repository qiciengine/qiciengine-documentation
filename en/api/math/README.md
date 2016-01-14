# qc.Math

## Description
Extens the class of `Math`.
This class represents a singleton object that can be accessed directly as `game.math`.

## Method
| Method | Description |
| ------------- |-------------|
| [fuzzyEqual](fuzzyEqual.md) | Two number are fuzzyEqual if their difference is less than epsilon |
| [fuzzyLessThan](fuzzyLessThan.md) | `a` is fuzzyLessThan `b` if it is less than b + epsilon   |
| [fuzzyGreaterThan](fuzzyGreaterThan.md) | `a` is fuzzyGreaterThan `b` if it is more than b - epsilon    |
| [fuzzyCeil](fuzzyCeil.md) | ceiling(val-epsilon)  |
| [fuzzyFloor](fuzzyFloor.md) | floor(val-epsilon)  |
| [average](average.md) | Averages all values passed to the function and returns the result.   |
| [shear](shear.md) | n mod 1 |
| [snapTo](snapTo.md) | Snap a value to nearest grid slice, using rounding.   |
| [snapToFloor](snapToFloor.md) | Snap a value to nearest grid slice, using floor.  |
| [snapToCeil](snapToCeil.md) | Snap a value to nearest grid slice, using ceil.    |
| [roundTo](roundTo.md) | Round to some place comparative to a `base`, default is 10 for decimal place. The `place` is represented by the power applied to `base` to get that place.    |
| [floorTo](floorTo.md) | Floor to some place comparative to a `base`, default is 10 for decimal place.  |
| [ceilTo](ceilTo.md) | Ceil to some place comparative to a `base`, default is 10 for decimal place.  |
| [angleBetween](angleBetween.md) | Find the angle of a segment from (x1, y1) -> (x2, y2).  |
| [angleBetweenY](angleBetweenY.md) | Note that the difference between this method and Math.angleBetween is that this assumes the y coordinate travels down the screen.  |
| [normalizeAngle](normalizeAngle.md) | Normalizes an angle to the [0,2pi) range.   |
| [reverseAngle](reverseAngle.md) |  Reverses an angle.|
| [maxAdd](maxAdd.md) |  Adds the given amount to the value, but never lets the value go over the specified maximum.   |
| [minSub](minSub.md) | Subtracts the given amount from the value, but never lets the value go below the specified minimum.      |
| [wrap](wrap.md) |Ensures that the value always stays between min and max, by wrapping the value around.      |
| [wrapValue](wrapValue.md) | Adds value to amount and ensures that the result always stays between 0 and max, by wrapping the value around.    |
| [wrapAngle](wrapAngle.md) | Keeps an angle value between -180 and +180; or -PI and PI if radians.   |
| [isOdd](isOdd.md) | Returns true if the number given is odd.   |
| [isEven](isEven.md) | Returns true if the number given is even. |
| [min](min.md) | Variation of Math.min that can be passed either an array of numbers or the numbers as parameters.   |
| [max](max.md) | Variation of Math.max that can be passed either an array of numbers or the numbers as parameters.     |
| [linear](linear.md) |  Calculates a linear (interpolation) value over t.    |
| [factorial](factorial.md) |  Calculates a factorial value .   |
| [getRandom](getRandom.md) |  Fetch a random entry from the given array.    |
| [distance](distance.md) | Returns the euclidian distance between the two given set of coordinates.       |
| [clamp](clamp.md) |Force a value within the boundaries by clamping `x` to the range `[a, b]`.    |
| [within](within.md) | Checks if two values are within the given tolerance of each other.          |
| [sign](sign.md) |  A value representing the sign of the value: -1 for negative, +1 for positive, 0 if value is 0.    |
| [degToRad](degToRad.md) | Convert degrees to radians.  |
| [radToDeg](radToDeg.md) | Convert radians to degrees.  |
| [random](random.md) | Returns a random real number between min and max |
| [uuid](uuid.md) | Returns a unique string |
| [id](id.md) | Returns next cookie |
| [invert](invert.md) | Invert matrix |
| [multiply](multiply.md) | Matrix multiply|
| [smoothDamp](smoothDamp.md) | Smooth damping |
