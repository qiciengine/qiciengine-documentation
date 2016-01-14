# qc.Slider
inherit [qc.ProgressBar](CProgressBar.md)

## Description
A standard slider that can be moved between a minimum and maximum value.

## Create a `Slider`
````
var slider = new qc.game.add.slider(parent);
````
See: [qc.GameObjectFactory#slider](slider.md)

## Variables
| Variable Name        |  Type     |   Description           |
| ------------- |-------------| -------------|
| canPursue | bool | Whether to allow the slider to pursue the click position |
| style | number | The manner in which progress should be indicated on the progress bar: Slider.STYLE_HORIZONTAL(From left to right), Slider.STYLE_VERTICAL(From up to bottom), Slider.STYLE_CIRCLE(Circle progressbar) |
| state | qc.UIState | State of the slider. |

__See also: [qc.ProgressBar](CProgressBar.md)__

## Manual
[Slider](http://docs.qiciengine.com/manual/Sample/Slider.html)