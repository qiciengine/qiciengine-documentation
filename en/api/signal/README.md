# qc.Signal

## Description
A Signal is an event dispatch mechansim than supports broadcasting to multiple listeners.

## Constructor
````
	var e = new qc.Signal();
````

## Methods
| Method | Description |
| ------------- |-------------|
| [add](add.md) | Add an event listener. |
| [has](has.md) | Check if a specific listener is attached. |
| [addOnce](addOnce.md) | Add a one-time listener - the listener is automatically removed after the first execution. |
| [remove](remove.md) | Remove a single event listener. |
| [removeAll](removeAll.md) | Remove all event listeners. |
| [dispatch](dispatch.md) | Dispatch / broadcast the event to all listeners. |

## Sample
````
	// Create a Signal.
	var e = new qc.Signal();

	// Add an event listener.
	e.add(function(p1, p2) {
		console.log('1. Receive event:', p1, p2);
	});
	e.addOnce(function(p1, p2) {
		console.log('2. Receive event:', p1, p2);
	});

	// Dispatch the event.
	e.dispatch('A', 'B');
	e.dispatch('C', 'D');
````