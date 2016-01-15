# AspectRatioFitter
qc.AspectRatioFitter脚本，用来保证其关联游戏对象的高度和宽度保持固定的比例。  
它可改变高度来适配宽度或改变宽度来适配高度等。  

## Ratio
宽高比参数，宽度除以高度的值
````javascript
aspectRatioFitter.ratio = 296 / 528;
````

## WIDTH_CONTROLS_HEIGHT
保证宽度不变，根据宽度和比例，自动调节高度。
````javascript
aspectRatioFitter.mode = qc.AspectRatioFitter.WIDTH_CONTROLS_HEIGHT;
````

## HEIGHT_CONTROLS_WIDTH
保证高度不变，根据高度和比例，自动调节宽度。
````javascript
aspectRatioFitter.mode = qc.AspectRatioFitter.HEIGHT_CONTROLS_WIDTH;
````

## FIT_IN_PARENT 
游戏对象的宽、高、位置和锚点将被自动调节，使得游戏对象矩形区域正好适合放入父亲对象的矩形区域，保证宽高比例，保持在父亲中心，一般游戏对象矩形区域会被父亲对象矩形区域包含。
````javascript
aspectRatioFitter.mode = qc.AspectRatioFitter.FIT_IN_PARENT;
````

## ENVELOPE_PARENT
游戏对象的宽、高、位置和锚点将被自动调节，使得游戏对象矩形区域填充满整个父亲对象的矩形区域，保证宽高比例，保持在父亲中心，一般游戏对象矩形区域会超出父亲对象矩形区域。
````javascript
aspectRatioFitter.mode = qc.AspectRatioFitter.ENVELOPE_PARENT;
````

## NONE
该模式下不做任何操作
````javascript
aspectRatioFitter.mode = qc.AspectRatioFitter.NONE;
````

## 示例
````javascript
var aspectRatioFitter = node.addScript('qc.AspectRatioFitter');
aspectRatioFitter.ratio = 296 / 528;
aspectRatioFitter.mode = qc.AspectRatioFitter.FIT_IN_PARENT;
````
![](images/aspectRatioExample.png)

## API
[AspectRatioFitter API](http://docs.zuoyouxi.com/api/components/AspectRatioFitter.html)

## Demo
[AspectRatioFitter Demo](http://engine.zuoyouxi.com/demo/Layout/aspect_ratio_fitter/index.html)
