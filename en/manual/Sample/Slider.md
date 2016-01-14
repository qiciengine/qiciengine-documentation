# Slider

qc.Slider allows the user to select a numeric value from a predetermined range by dragging. qc.Slider inherits from qc.ProgressBar, so a Slider object has all the features of [ProgressBar](ProgressBar.html).
![](images/slider1.png)

## Properties on Inspector
![](images/slider2.png)

* __Sliders__: object of UIImage, node.sliders = sliders;
* __Style__: Support 3 styles as below, node.style = Sliders.STYLE_HORIZONTAL;
	* Horizontal Sliders - Sliders.STYLE_HORIZONTAL
	* Vertical Sliders - Sliders.STYLE_VERTICAL
	* Circle Sliders - Sliders.STYLE_CIRCLE
* __Min Value__: the min value, node.minValue = 0.0;
* __Max Value__: the max value, node.maxValue = 1.0;
* __Value__: current value, node.value = 0.3;
* __Fixed Size__: The silders's size percentage of the parent rectangle, 1.0 as occupy the whole rectangle, negative value as not fixed size, node.fixedSize = 0.3;
* __Can Pursue__: When canPurse is checked, sliders will automatically move to the place where the user click, node.canPursue = true;
* __Clip Sliders__: Whether to clip silders or not. Normally need to be clipped when as circle style, node.clipSliders = true;
* __Start Radian__: The start radian, valid when circle style, node.startRadian = Math.PI;
* __End Radian__: The end radian, valid when circle style, node.endRadian = Math.PI;
* __Start Angle__: The start angle, valid when circle style, node.startAngle = 90;
* __End Angle__: The start angle, valid when circle style, node.endAngle = 90;
* __State__: Slider has a state property that can be in 3 types of values as below:
	* qc.UIState.NORMAL - The normal state
	* qc.UIState.PRESSED - The pressed state
	* qc.UIState.DISABLED - The state that the slider will not respond to input


````javascript
var slider = new qc.Slider(game, parent);

slider.interactive = true;
slider.width = 160;
slider.height = 20;

var slidingArea = game.add.node(slider);
slidingArea.name = 'slidingArea';
slidingArea.setAnchor(new qc.Point(0, 0), new qc.Point(1, 1));
slidingArea.setStretch(0, 0, 0, 0);
slidingArea.pivotX = slidingArea.pivotY = 0.5;

var sliders = game.add.image(slidingArea);
sliders.name = 'sliders';
sliders.setAnchor(new qc.Point(0.5, 0.5), new qc.Point(0.5, 0.5));
sliders.setStretch(0, 0, 0, 0);
sliders.pivotX = sliders.pivotY = 0.5;

slider.sliders = sliders;

slider.texture = game.assets.find('__builtin_resource__');
slider.frame = 'button.png';
slider.imageType = qc.UIImage.IMAGE_TYPE_SLICED;
slider.height = 15;
slider.value = 0.5;

sliders.texture = game.assets.find('__builtin_resource__');
sliders.frame = 'button.png';
sliders.imageType = qc.UIImage.IMAGE_TYPE_SLICED;
sliders.height = 15;

````

## API
[Slider API](http://docs.qiciengine.com/api/gameobject/CSlider.html)

## Demo
[Slider Demo](http://engine.qiciengine.com/demo/Slider/slider_todo/index.html)
