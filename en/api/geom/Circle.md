# qc.Circle

## Descriptions
Circle.

## Constructor
````
	// Creates a new Circle object with the center coordinate specified by the x and y parameters and the diameter specified by the diameter parameter.
	// If you call this function without parameters, a circle with x, y, diameter and radius properties set to 0 is created.
	var circle = new qc.Circle(0, 0, 1);
````

## Variables
| Variable Name        |   Type       |  Description           |
| ------------- |-------------|-------------|
| x | number | The x coordinate of the center of the circle. |
| y | number | The y coordinate of the center of the circle. |
| diameter | number | The diameter of the circle. |
| radius | number | The radius of the circle. |

## Example
````
	// Returns the distance from the center of the Circle object to the given object
	circle.distance({ x: 5, y: 6});
````
