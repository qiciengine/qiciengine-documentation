# Point

## Description
A Point object represents a location in a two-dimensional coordinate system, where x represents the horizontal axis and y represents the vertical axis.

## Constructor
````
	var pt = new qc.Point(2, 3);
````

## Variables
| Variable Name      |   Type       |  Description           |
| ------------- |-------------|-------------|
| x | number | The horizontal position of this Point. |
| y | number | The vertical position of this Point. |

## Example
````
	// Returns the distance of this Point object to the given object (can be a Circle, Point or anything with x/y properties)
	var pt = new qc.Point(0, 0);
	pt.distance(new Point(100, 50));
	pt.distance({ x: 5, y: 8 });

	// Determines whether the given objects x/y values are equal to this Point object.
	if (pt.equals(new qc.Point(1, 1))) {
		console.log('Yes.');
	}

	// Returns the angle between this Point object and another object with public x and y properties.
	// In radians
	pt.angle(new qc.Point(1, 1), false);

	// Returns the angle between this Point object and another object with public x and y properties.
	// In degrees
	pt.angle(new qc.Point(1, 1), true);

	// Rotates this Point around the x/y coordinates given to the desired angle.
	pt.rotate(1, 2, Math.PI/2, false);
	pt.rotate(1, 2, 90, true);
````
