# qc.Toggle
inherit [qc.Node](CNode.md)

## 描述
开关对象。

## 创建 Toggle
````
var toggle = new qc.game.add.toggle(parent);
````

## 变量
| 变量名        |  类型     |   作用           |
| ------------- |-------------| -------------|
| background |  qc.UIImage | 背景图片 |
| checkMark |  qc.UIImage | 选中标记图片 |
| text |  qc.Text | 挂载在开关上的文本组件 |
| on |  bool | 开关是否处于开的状态 |
| state | number | 开关的点击状态，包括：UIState.NORMAL（正常状态）、UIState.PRESSED（按下状态）、UIState.DISABLED（不可用） |

## 事件
|   事件名      |     作用       |
| ------------- |-------------|
| onValueChange | 开关的 on 值发生变化的事件
| onStateChange | 开关的 state 值发生变化的事件 |

## 参考手册
[开关和开关组](http://docs.zuoyouxi.com/manual/Sample/Toggle.html)