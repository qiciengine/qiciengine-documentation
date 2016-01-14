# [qc.Keyboard](Keyboard.md).isAnyKeyDown

## Prototype
* boolean isAnyKeyDown(void)

## Description
Check whether any key is pressed in current frame.
Note that it return ture only while key is pressed in current frame, if key is still pressed in next frame, it will return false.

## Example
````
	if (game.input.keyboard.isAnyKeyDown()) {
		console.log('Key down.');
	}
````
