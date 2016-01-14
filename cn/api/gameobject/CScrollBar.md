# qc.ScrollBar
inherit [qc.UIImage](CUIImage.md)

## 描述
滚动条控件，用于滚动ScrollView视图，和显示当前滚动偏移，该控制主要显示滚动条背景，需要设置滑块。

## 创建 ScrollBar
````
var scrollbar = new qc.game.add.scrollbar(parent);
````
参见 [qc.GameObjectFactory#scrollBar](scrollBar.md)

## 变量
| 变量名        |  类型     |   作用           |
| ------------- |-------------| -------------|
| sliders | [qc.Slider](CSlider.md) | 滑块对象 |
| direction | number | 滚动条的滑动方向 |
| value | number | 当前滑动的值，[0-1] |
| size | number | 滑块长度和滑块区域的比例,(0,1], 滑块最小5个像素 |
| numberOfStep | number | 滑动时，滑块从 0 到 1 的步数 |
| stepSize | number | 滚动时每步改变的值 |
| fixSlidersSize | bool | 是否固定滑条大小 |

## 事件
| 事件名  | 作用 |
| ------------- |-------------|
| onValueChange | 当滑块值发生变化时的事件 |

## 参考手册
[滚动条](http://docs.zuoyouxi.com/manual/Sample/ScrollView.html)