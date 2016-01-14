# [qc.Timer](README.md).loop

## Prototype
* qc.TimerEvent loop(number delay, function cb=, object context, ...*)

## Parameters
| Parameter | Type | Description |
| ------------- | ------------- | -------------|
| delay | number | The number of milliseconds that should elapse before the Timer will call the given callback. |
| cb | function | The callback that will be called when the Timer event occurs. |
| context | undefined、object | The context in which the callback will be called. |
| ...* | ...* | Additional arguments that will be supplied to the callback. |

## Description
Adds a new looped Event

## Example
````
	var t = game.timer.loop(1000, function() {
		console.log('Timer trigger');
	});

	game.timer.remove(t);
````
