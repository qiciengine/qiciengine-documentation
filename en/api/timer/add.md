# [qc.Timer](README.md).add

## Prototype
* qc.TimerEvent add(number delay=, function cb, object context, ...*)

## Parameters
| Parameter | Type | Description |
| ------------- | ------------- | -------------|
| delay | number | The number of milliseconds that should elapse before the callback is invoked. |
| cb | function | The callback that will be called when the Timer event occurs. |
| context | undefined、object | The context in which the callback will be called. |
| ...* | ...* | Additional arguments that will be supplied to the callback. |

## Description
Create a new timer event.

## Example
````
	var t = game.timer.add(1000, function() {
		console.log('Timer trigger.');
	})
````
