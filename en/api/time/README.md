# qc.Time

## Description
This is the core internal game clock.  
It manages the elapsed time and calculation of elapsed values, used for game object motion and tweens.  
This class represents a singleton object that can be accessed directly as `game.time`.  

## Variables
| Variable Name  |  Type | Description |
| ------------- |-------------|
| game | [qc.Game](../Game/README.md) | The local game reference. |
| frameRate | int | The desired frame rate of the game. |
| now | int | Read only. The `Date.now()` value |
| scaledTime  | int | Read only. The number of milliseconds that have elapsed since the game was started. Affected by `timeScale` |
| fixedTime | int | Read only. The number of milliseconds that have elapsed since the game was started. | 
| timeScale | number | Scaling factor to make the game move smoothly in slow motion. 1.0=normal speed; 2.0=half speed. |
| deltaTime | number | Elapsed time since the last time update, in milliseconds.|

## Manual
[Time](http://docs.qiciengine.com/manual/Time/index.html)