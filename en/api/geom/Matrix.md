# Matrix

## Description
The Matrix class is now an object, which makes it a lot faster, here is a representation of it :
````
	| a | b | tx|
	| c | d | ty|
	| 0 | 0 | 1 |
````

## Constructor
````
	var m = new qc.Matrix();
````

## Variables
| Variable Name    |   Type       |  Description           |
| ------------- |-------------|-------------|
| a | number | a. Default:1 |
| b | number | b. Default:0 |
| c | number | c. Default:0 |
| d | number | d. Default:1 |
| tx | number | tx. Default:0 |
| ty | number | ty. Default:0 |

## Example
````
	// Creates a Matrix object based on the given array. The Element to Matrix mapping order is as follows:
	//   a = array[0]
    //   b = array[1]
    //   c = array[3]
    //   d = array[4]
    //   tx = array[2]
    //   ty = array[5]
	m.fromArray([0, 0, 1, 0, 0, 1]);

	// Get a new position with the current transformation applied.
	// Can be used to go from a child's coordinate space to the world coordinate space. (e.g. rendering)
	m.apply(new qc.Point(5, 4));

	// Get a new position with the inverse of the current transformation applied.
	// Can be used to go from the world coordinate space to a child's coordinate space. (e.g. input)
	m.applyInverse(new qc.Point(5, 4));

	// Translates the matrix on the x and y.
	m.translate(1, 2);

	// Applies a scale transformation to the matrix.
	m.scale(1, 1);

	// Applies a rotation transformation to the matrix.
	m.rotate(Math.PI / 2);
````
