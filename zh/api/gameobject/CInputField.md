# qc.InputField
inherit [qc.UIImage](CUIImage.md)

## 描述
文本输入框控件。

## 创建 InputField
````
    var inputField = new qc.game.add.inputField(parent);
````

## 属性
|  属性名  |  类型  |  作用   |
| ---------- | --------- | ---------- |
| state | number  | 输入框的状态，包含:UIState.NORMAL（正常）、UIState.PRESSED（按下）、UIState.DISABLED（不可用） |
| lineType | number | 编辑框是多行or单行，InputField.SINGLE_LINE（单行）、InputField.MULTI_LINE（多行） |
| contentType | number | 输入框的类型，包括有：InputField.STANDARD（任意字符串）、InputField.INT（整数）、InputField.NUMBER（数字）、InputField.TEL（电话号码）、InputField.EMAIL（电子邮件）、InputField.PASSWORD（密码） |
| text | string | 编辑框的内容 |
| placeholderText | string | 占位符字符串 |
| characterLimit | number | 输入字符的限制。-1表示不受限 |
| overflow | bool | 超出部分是否要裁切掉，默认为true |
| isFocused | bool | 是否处于编辑状态 |
| textComponent | qc.Node | 关联的输入文本对象 |
| placeholder | qc.Node | 关联的占位符文本对象 |

## 事件
|   事件名      |     作用       |
| ------------- |-------------|
| onValueChange | 状态发生改变的事件 |
| onStateChange | 文本发生变化的事件 |


## 参考手册
[输入框](http://docs.zuoyouxi.com/manual/Sample/InputField.html)