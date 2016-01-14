# Line

## Description
Line.

## Constructor
````
	// Creates a new Line object with a start and an end point.
	var line = new qc.Line(0, 0, 1, 1);
````

## Variables
| Variable Name      |   Type       |  Description           |
| ------------- |-------------|-------------|
| start | [qc.Point](Point.md) | The start point of the line. |
| end | [qc.Point](Point.md) | The end point of the line. |
| length | number | Read only. The length of the line in pixels. |
| angle | number | Read only. The angle of the line |
| width | number | Read only. The width of this bounds of this line. |
| height | number | Read only. The height of this bounds of this line. |

## Example
````
	var line = new qc.Line(0, 0, 0, 0);

	// Sets this line to start at the given `x` and `y` coordinates and
	// for the segment to extend at `angle` for the given `length`.
	line.fromAngle(0, 0, Math.PI/2, 100);

	// Returns the reflected angle between two lines.
	// This is the outgoing angle based on the angle of this line and the normalAngle of the given line.
	line.reflect(new qc.Line(1, 1, 5, 4));

	// Tests if the given coordinates fall on this line.
	// See pointOnSegment to test against just the line segment.
	line.pointOnLine(1, 5);
````
