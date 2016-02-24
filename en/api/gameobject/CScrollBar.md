# qc.ScrollBar
inherit [qc.UIImage](CUIImage.md)

## Description
A standard scrollbar with a variable sized handle that can be dragged between 0 and 1.

## Create a `ScrollBar`
````
var scrollbar = new qc.game.add.scrollbar(parent);
````
See: [qc.GameObjectFactory#scrollBar](scrollBar.md)

## Variables
| Variable Name        |  Type     |   作用           |
| ------------- |-------------| -------------|
| sliders | [qc.Slider](CSlider.md) | The reference to slider Node. |
| direction | number | The direction of the scrollbar from minimum to maximum value. |
| value | number | The current value of the scrollbar, between 0 and 1. |
| size | number | The size of the scrollbar handle where 1 means it fills the entire scrollbar. |
| numberOfStep | number | The number of steps to use for the value. A value of 0 disables use of steps. |
| stepSize | number | The Step size. |
| fixSlidersSize | bool | The size of slider is fixed. |
| autoHide | bool | Whether hide the scrollbar automatically when the slider size is equal to slide area. |

## Events
| Event  | Description |
| ------------- |-------------|
| onValueChange | When the value is changed, this event is triggered. |

## Manual
[ScrollBar](http://docs.qiciengine.com/manual/Sample/ScrollView.html)