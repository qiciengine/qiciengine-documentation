# 动作属性定义
[动作编辑器](http://docs.zuoyouxi.com/manual/Action/ActionEditor.html) 的左侧动作属性视图中每个动作属性都对应一个宏定义，每个动作属性展开后有哪些属性，也在这里说明。  
![](image/actionDef.png)  
_其中 Position 为动作属性，x、y 为 Position 下的具体属性_  
在代码中，需要修改指定属性的关键帧曲线数据时，可以使用 [qc.Action](Action.md).[setData](setData.md) 方法，该方法使用 path、propertyId、attrib 三个参数来定位指定对象的指定动作属性的指定具体属性。
其中 path 见 [setData](setData.md) 中的说明；propertyId 为动作属性的[宏定义](#宏定义)，以上图为例，为 qc.PROP_POSITION；attrib 为动作属性的[具体属性](#动作属性对应的属性列表)，以上图为例，为 x 和 y。  


## 宏定义
````javascript
qc.PROP_POSITON = 1;               // Position
qc.PROP_ROTATION = 2;              // Rotation
qc.PROP_ALPHA = 3;                 // Alpha
qc.PROP_SCALE = 4;                 // Scale
qc.PROP_COLOR_TINT = 5;            // ColorTint
qc.PROP_VISIBLE = 6;               // Visible
qc.PROP_SIZE = 7;                  // Size
qc.PROP_SKEW = 8;                  // Skew
qc.PROP_TEXTURE = 9;               // Texture
qc.PROP_ANIMATION = 10;            // Animation
qc.PROP_COLOR = 11;                // Color
qc.PROP_TEXT = 12;                 // Text
qc.PROP_PIVOT = 13;                // Pivot
qc.PROP_ANCHORED_POSITION = 14;    // AnchoredPosition
qc.PROP_TOGGLE_ON = 15;            //  ToggleOn
qc.PROP_SCROLLBAR_VALUE = 16;      // ScrollBarValue 
qc.PROP_SCROLLVIEW_POSITION = 17;  // ScrollViewPosition
qc.PROP_PROGRESSBAR_VALUE = 18;    // ProgressBarValue
qc.PROP_SLIDER_VALUE = 19;         // SliderValue
qc.PROP_SOUND = 20;                // Sound
qc.PROP_DOM_INNERHTML = 21;        // DomInnerHTML
qc.PROP_TILEMAP_POSITION = 22;     // TilemapPosition
````
每个宏定义都有注释的字符串，注释的字符串为 [动作编辑器](http://docs.zuoyouxi.com/manual/Action/ActionEditor.html) 左侧动作属性视图中显示的动作属性名。如上图中的 Position。  
  
## 动作属性对应的属性列表  
在 [动作编辑器](http://docs.zuoyouxi.com/manual/Action/ActionEditor.html) 左侧动作属性视图中，将动作属性展开，可以看到具体的属性。  
具体属性的名字可在 [动作编辑器](http://docs.zuoyouxi.com/manual/Action/ActionEditor.html) 左侧动作属性视图中直接看到。如上图所示，Position 动作属性包含了 x 和 y 两个具体属性。  
  
以下列出当前所有动作属性包括哪些具体属性：
````javascript
qc.PROP_POSITON : { 'x', 'y' }
qc.PROP_ROTATION : { 'rotation' }
qc.PROP_ALPHA : { 'alpha' }
qc.PROP_SCALE : { 'scaleX', 'scaleY' }
qc.PROP_COLOR_TINT : { 'colorTint' }
qc.PROP_VISIBLE : { 'visible' }
qc.PROP_SIZE : { 'width', 'height' }
qc.PROP_SKEW : { 'skewX', 'skewY' }
qc.PROP_TEXTURE : { 'texture' }
qc.PROP_ANIMATION : { 'defaultAnimation' }
qc.PROP_COLOR : { 'color' }
qc.PROP_TEXT : { 'text' }
qc.PROP_PIVOT : { 'pivotX', 'pivotY' }
qc.PROP_ANCHORED_POSITION : { 'anchoredX', 'anchoredY' }
qc.PROP_TOGGLE_ON : { 'on' }
qc.PROP_SCROLLBAR_VALUE : { 'value' }
qc.PROP_SCROLLVIEW_POSITION : { 'horizontalNormalizedPosition', 'verticalNormalizedPosition' }
qc.PROP_PROGRESSBAR_VALUE : { 'value' }
qc.PROP_SLIDER_VALUE : { 'value' }
qc.PROP_SOUND : { 'audio', 'isPlaying' }
qc.PROP_DOM_INNERHTML : { 'innerHTML' }
qc.PROP_TILEMAP_POSITION : { 'scrollX', 'scrollY' }
````
