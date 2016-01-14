# qc.Timer

## Description
A Timer is a way to create small re-usable (or disposable) objects that wait for a specific moment in time,
and then run the specified callbacks.  
This class represents a singleton object that can be accessed directly as `game.timer`.    

__Be careful: The timer is affected by `game.time.timeScale`__

## Methods
| Method     | Description |
| ------------- |-------------|
| [add](add.md) | Create a new timer event.  |
| [loop](loop.md) | Adds a new looped Event. |
| [remove](remove.md) | Removes a pending TimerEvent from the queue. |
