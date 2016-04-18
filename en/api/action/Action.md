# qc.Action

## Description  
qc.Action is abstract of _Action Clip_ file. It is responsible for controlling _Action Clip_.

## Variables
| Variable Name       | Type   |    Description        |
| ------------- |-------------|-------------|
| game            | qc.Game          | Game instance        |
| targetObject    | qc.Node  | Action's target object who play this action.       |
| targetLocked    | boolean   | Whether targetObject is locked.          |
| samples  | int       | Frame amount per second.      |
| duration | int | The duration of single loop.              |
| speed | int | The speed of action.              |
| loop           | boolean          | Whether action is loop.          |

## Event
| Event Name             | Description               |
| -------------   | -------------    |
| onFinished            |   When action finished, this event is triggered.      |
| onLoopFinished            |   When a single loop is finished, this event is triggered.   |

## Methods
| Method | Description |
| -------------  | ------------- |
| [setData](setData.md)  | Set data for specific animated property of _Action Clip_ .     |

## Manual
[Action](http://docs.qiciengine.com/manual/Action/ActionEditor.html)
