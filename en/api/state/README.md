# qc.SceneManager

## Description
Downloads or loads the scene.  
This class represents a singleton object that can be accessed directly as `game.scene`.   

## Variables
| Variable | Type | Description |
| ------------- |-------------|-------------|
| game | [qc.Game](../game/README.md) | The local game reference. |
| entry | string | The entry scene's name. |
| list | Array | The scene list of the game. |
| loading | boolean | Is the scene in loading? |
| current | string | The current running scene. |

## Events
| Event | Description |
| ------------- |-------------|
| onStartLoad | When the scene starts loading, this event is triggered. |
| onEndLoad | When the scene loads complete, this event is triggered. |

## Methods
| Method | Description |
| ------------- |-------------|
| [download](download.md) | Downloads a scene. |
| [load](load.md) | Loads a scene. |
