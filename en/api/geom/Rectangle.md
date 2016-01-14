# Rectangle

## Description
Rectangle.

## Constructor
````
	// Creates a new Rectangle object with the top-left corner specified by the x and y parameters
	// and with the specified width and height parameters.
	// If you call this function without parameters, a Rectangle with x, y, width,
	// and height properties set to 0 is created.
	var rect = new qc.Rectangle(0, 0, 1, 2);
````

## Variables
| Variable Name   |   Type       |  Description           |
| ------------- |-------------|-------------|
| x | number | The x coordinate of the top-left corner of the Rectangle. |
| y | number | The y coordinate of the top-left corner of the Rectangle. |
| width | number | The width of the Rectangle. Should always be either zero or a positive value. |
| height | number | The height of the Rectangle. Should always be either zero or a positive value. |
| centerX | number | The x coordinate to place the center of the Rectangle at. |
| centerY | number | The y coordinate to place the center of the Rectangle at. |

## Example
````
	// Centers this Rectangle so that the center coordinates match the given x and y values.
	rect.centerOn(1，1);

	// Determines whether the specified coordinates are contained within the region defined by this Rectangle object.
	rect.contains(1, 1);
````
