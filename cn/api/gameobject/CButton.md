# qc.Button
inherit [qc.UIImage](CUIImage.md)

## 描述
按钮，继承自 [UIImage](CUIImage.md)，默认会挂载 [qc.TransitionBehaviour](../components/TransitionBehaviour.md) 组件，用于支持交互中时普通、按下、不可用状态下的处理。

## 变量
| 变量名        |   类型       |  作用           |
| ------------- |-------------|-------------|
| state | int  |  当前按钮的状态，包括：UIState.NORMAL（正常状态）、UIState.PRESSED（按下状态）、UIState.DISABLED（不可用） |
| text | [qc.UIText](CUIText.md) | 按钮上的文本对象 |
| supportNativeEvent | boolean | 是否响应浏览器直接事件 |

## 事件
|   事件名      |     作用       |
| ------------- |-------------|
| onStateChange | 按钮状态发生变化的事件 |
| onNativeClick | native 点击事件 |

## 参考手册
[按钮](http://docs.zuoyouxi.com/manual/Sample/Button.html)