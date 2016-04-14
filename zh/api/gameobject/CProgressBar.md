# qc.ProgressBar
inherit [qc.UIImage](CUIImage.md)

## 描述
滑动条控件

## 创建 ProgressBar
````
var progressBar = new qc.game.add.progressBar(parent);
````
参见 [qc.GameObjectFactory#progressBar](progressBar.md)

## 变量
| 变量名        |  类型     |   作用           |
| ------------- |-------------| -------------|
| style | number | 显示样式，包括 ProgressBar.STYLE_HORIZONTAL（水平进度条）、ProgressBar.STYLE_VERTICAL（竖直进度条）、ProgressBar.STYLE_CIRCLE（圆形进度条） |
| sliders | [qc.Slider](CSlider.md) | 滑块对象 |
| indeterminable | bool | 是否是不确定类型，如果无法明确知道进度或者结束值，则使用不确定类型，进度条将循环播放 |
| minValue | number | 当前进度条的最小值 |
| maxValue | number | 当前进度条的最大值 |
| length | number |  只读，进度条的长度（值为 maxValue - minValue） |
| value | number | 当前的进度值 |
| loopTime | number | 循环时间，当 indeterminable 为 true 时候生效 |
| numberOfStep | number | 在循环播放时，从0到max的步数，仅当indeterminable为true时有效, 小于等于0时，按实际值显示 |
| stepSize | number | 步进距离 |
| fixedSize | number | 滑块的大小，值为占整个进度条区域的百分比，1为整个区域, < 0 时表示不限制大小 |
| clipSliders | bool | 是否裁切滑块 |
| showMode | number | 显示模式，ProgressBar.SHOW_PROCESSED（显示进行了的部分）、ProgressBar.SHOW_REMAINED（显示剩余的部分 ）|
| reverse | bool | 是否反向显示 |
| startRadian | number | 开始的弧度，仅当style为STYLE_CIRCLE时有效 |
| endRadian | number | 结束的弧度，仅当style为STYLE_CIRCLE时有效，endRadian > startRadian && endRadian <= startRadian + Math.PI * 2 |
| startAngle | number | 开始的角度，仅当style为STYLE_CIRCLE时有效 |
| endAngle | number | 结束的角度，仅当style为STYLE_CIRCLE时有效，endRadian > startRadian && endRadian <= startRadian + Math.PI * 2 |
| showRadian | number | 只读，当前显示的弧度 |

## 事件
| 事件名 | 说明 |
| -------- | ------- |
| onValueChange | 滚动值发生变更的时候派发 |

## 参考手册
[进度条](http://docs.zuoyouxi.com/manual/Sample/ProgressBar.html)