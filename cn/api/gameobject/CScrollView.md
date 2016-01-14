# qc.ScrollView
inherit [qc.Node](CNode.md)

## 描述
滚动视图，用于在一个指定的小区域内显示较大的内容。

## 创建 ScrollView
````
var scrollView = new qc.game.add.scrollView(parent);
````

## 变量
| 变量名        |  类型     |   作用           |
| ------------- |-------------| -------------|
| canHorizontal | bool | 是否响应水平滑动 |
| canVertical | bool | 是否响应垂直滑动 |
| movementType | number | 边界限制类型，ScrollView.MOVEMENT_UNRESTRICTED（滚动区域无限制）、ScrollView.MOVEMENT_ELASTIC（滚动区域有限制，但可以超越边界，之后被拖回）、ScrollView.MOVEMENT_CLAMPED（滚动区域有限制，无法超过边界） |
| elasticity | number | 当 moveMentType 为 MOVEMENT_ELASTIC 时生效，用于表示复位速度 |
| inertia | bool | 是否惯性滑动 |
| decelerationRate | number | 惯性滑动的减速参数 |
| scrollSensitivity | number | 响应滚动时的倍率 |
| propagationScroll | bool | 是否向上传递滚动事件 |
| content | [qc.Node](CNode.md） | 需要滚动显示的内容 |
| horizontalScrollBar | [qc.ScrollBar](CScrollBar.md) or null | 水平滚动条，该 ScrollBar 的滑动会影响 ScrollView 的水平值，反之亦然 |
| horizontalNormalizedPosition | number | 水平方向滚动的比例（0 - 1） |
| verticalScrollBar | [qc.ScrollBar](CScrollBar.md) or null | 垂直滚动条，该 ScrollBar 的滑动会影响 ScrollView 的纵向值，反之亦然 |
| verticalNormalizedPosition | number | 垂直方向滚动的比例（0 - 1） |

## 方法
| 方法名 | 作用 |
| ------------- |-------------|
| [setNormalizedPosition](sv_setNormalizedPosition.md) | 设置指定方向上的滚动值  |

## 事件
| 事件名  | 作用 |
| ------------- |-------------|
| onValueChange | 偏移值发生变化时调用 |

## 参考手册
[滚动视图](http://docs.zuoyouxi.com/manual/Sample/ScrollView.html)