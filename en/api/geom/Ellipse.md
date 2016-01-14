# qc.Ellipse

## Description
Ellipse: A curve on a plane surrounding two focal points.

## Constructor
````
	var ellipse = new qc.Ellipse(0, 0, 1, 2);
````

## Variables
| Variable        |   Type       |  Description           |
| ------------- |-------------|-------------|
| x | number | The X coordinate of the upper-left corner of the framing rectangle of this ellipse. |
| y | number | The Y coordinate of the upper-left corner of the framing rectangle of this ellipse. |
| width | number | The overall width of this ellipse. |
| height | number | The overall height of this ellipse. |

## Example
````
	// Returns the distance from the center of the Ellipse object to the given object
	ellipse.distance({ x: 5, y: 6});

	// Return true if the given x/y coordinates are within this Ellipse object.
	ellipse.contains(1, 1);
````
