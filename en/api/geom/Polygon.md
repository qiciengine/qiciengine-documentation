# Polygon

## Description
Polygon.

## Constructor
````
	var polygon = new qc.Polygon(new qc.Point(0, 0), new qc.Point(1, 1), new qc.Point(1, 4));
````

## Variables
| Variable Name     |   Type       |  Description           |
| ------------- |-------------|-------------|
| area | number | The area of this Polygon. |
| closed | boolean | Is the Polygon closed or not? |
| points | array | An array of Points that make up this Polygon. |

## Example
````
	// Checks whether the x and y coordinates are contained within this polygon.
	polygon.contains(1, 1);
````
