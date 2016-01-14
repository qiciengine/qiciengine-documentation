# [qc.Touch](Touch.md).isTouchStart

## Prototype
* boolean isTouchStart(id:int)

## Paramters
| Paramter | Type | Description |
| --- | ---- | ---- |
| id | number | see : [qc.Touch](touch.md) |

## Description
 Check whether a specified touch start

## Example
````
	if (game.input.touch.isTouchStart(qc.Touch.MAIN)) {
		console.log('Main Touch.');
	}
````
