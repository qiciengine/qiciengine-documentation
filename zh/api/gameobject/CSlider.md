# qc.Slider
inherit [qc.ProgressBar](CProgressBar.md)

## 描述
滑动条控件

## 创建 Slider
````
var slider = new qc.game.add.slider(parent);
````
参见 [qc.GameObjectFactory#slider](slider.md)

## 变量
| 变量名        |  类型     |   作用           |
| ------------- |-------------| -------------|
| canPursue | bool | 是否允许滑块追赶点击位置 |
| style | number | 滑条类型，包含：Slider.STYLE_HORIZONTAL（水平进度条）、Slider.STYLE_VERTICAL（竖直进度条）、Slider.STYLE_CIRCLE（圆形进度条）|
| state | qc.UIState | 滑块的状态 |

__继承的属性请详见[qc.ProgressBar](CProgressBar.md)__

## 参考手册
[拉条](http://docs.zuoyouxi.com/manual/Sample/Slider.html)