# qc.ProgressBar
inherit [qc.UIImage](CUIImage.md)

## Description
Represents a progress bar control.

## Create a `ProgressBar`
````
var progressBar = new qc.game.add.progressBar(parent);
````
See: [qc.GameObjectFactory#progressBar](progressBar.md)

## Variables
| Variable Name     |  Type     |   Description           |
| ------------- |-------------| -------------|
| style | number | The manner in which progress should be indicated on the progress bar: ProgressBar.STYLE_HORIZONTAL(From left to right), ProgressBar.STYLE_VERTICAL(From up to bottom), ProgressBar.STYLE_CIRCLE(Circle progressbar) |
| sliders | [qc.Slider](CSlider.md) | The referebce to the slider Node. |
| indeterminable | bool | Whether the ProgressBar shows actual values or generic, continuous progress feedback. |
| minValue | number | The minimum allowed value of the progressBar. |
| maxValue | number | The maximum allowed value of the progressBar. |
| length | number |  Read only. = maxValue - minValue |
| value | number | The current value of the progressBar. |
| loopTime | number | When indeterminable=true, loopTime works.  |
| numberOfStep | number | Then number of steps from 0 to max when play in loop. It is only effect when indeterminable variable is true. |
| stepSize | number | The size of each step |
| fixedSize | number | The size of the slider. Value is percent. 1: full area |
| clipSliders | bool | Whether to cut slider |
| showMode | number | Show mode. You can take the following two values: ProgressBar.SHOW_PROCESSED(show processed part), and ProgressBar.SHOW_REMAINED(show left part)|
| reverse | bool | Whether to show reverse |
| startRadian | number | The start radian. It is only effect when style is STYLE_CIRCLE. |
| endRadian | number | The end radian. It is only effect when style is STYLE_CIRCLE. |
| startAngle | number | The start angle. It is only effect when style is STYLE_CIRCLE. |
| endAngle | number |  The end angle. It is only effect when style is STYLE_CIRCLE. |
| showRadian | number |Read only. current radian |

## Events
| Event | Description |
| -------- | ------- |
| onValueChange | When the value of progressBar changes, this event is triggered. |

## Manual
[ProgressBar](http://docs.qiciengine.com/manual/Sample/ProgressBar.html)