# [qc.Mouse](Mouse.md).isMouseDown

## Prototype
* boolean isMouseDown(id: int);

## Paramters
| Paramter | Type | Description |
| --- | ---- | ---- |
| id | number | see : [qc.Mouse](Mouse.md) |

## Description
Check whether a specified mouse button is pressed.

## Example
````
	if (game.input.mouse.isMouseDown(qc.Mouse.BUTTON_LEFT)) {
		console.log('Left mouse button pressed.');
	}
````

