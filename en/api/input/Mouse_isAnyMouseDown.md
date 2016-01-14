# [qc.Mouse](Mouse.md).isAnyMouseDown

## Prototype
* boolean isAnyMouseDown(void);

## Description
Check whether any mouse is pressed in current frame.
Note that it return ture only while mouse is pressed in current frame, if mouse is still pressed in next frame, it will return false.

## Example
````
	if (game.input.mouse.isAnyMouseDown()) {
		console.log('Mouse pressed.');
	}
````
