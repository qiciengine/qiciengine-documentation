# qc.Toggle
inherit [qc.Node](CNode.md)

## Description
A standard toggle that has an on / off state.

## Create a `Toggle`
````
var toggle = new qc.game.add.toggle(parent);
````

## Variables
| Variable   |  Type     |   Description    |
| ------------- |-------------| -------------|
| background |  qc.UIImage | The reference of background image. |
| checkMark |  qc.UIImage | The reference of checking mark image. |
| text |  qc.Text | The reference of text node. |
| on |  bool | Is the toggle on. |
| state | number | The state of toggle: UIState.NORMAL, UIState.PRESSED, UIState.DISABLED |

## Events
|   Event      |     Description     |
| ------------- |-------------|
| onValueChange | When on is changed, this event is triggered. |
| onStateChange | When state is changed, this event is triggered. |

## Manual
[Toggle And ToggleGroup](http://docs.qiciengine.com/manual/Sample/Toggle.html)