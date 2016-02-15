# qc.Dropdown
inherit [qc.UIImage](CUIImage.md)

## 描述
下拉列表控件。  

## 变量
| 变量名        |   类型       |  描述           |
| ------------- |-------------|-------------|
| state | int  |  当前按钮的状态，包括：UIState.NORMAL（正常状态）、UIState.PRESSED（按下状态）、UIState.DISABLED（不可用） |
| captionImage | qc.UIImage | 显示当前选中的图片选项。 |
| captionText | qc.UIText | 显示当前选中的文本选项。 |
| item | qc.Node | 用来显示选项的节点。 |
| options | Array | 选项列表。选项可以是文本类型，也可以指定为图片类型。 |
| template | qc.Node | 下拉框的显示模板。 |
| value | int | 当前第几个选项被选中了。0表示第一个，1表示第二个，以此类推。 |

## 事件
|   事件名      |     描述       |
| ------------- |-------------|
| onStateChange | 当下拉框的状态发生变化了，此事件被派发。 |
| onValueChange | 当选项发生变化了，此事件被派发。 |

## 方法
| 方法名 | 描述 |
| ------------- |-------------|
| [addOptions](dropdown_addOptions.md) | 添加多个选项。|
| [clearOptions](dropdown_clearOptions.md) | 所有选项清空。 |
| [show](dropdown_show.md) | 显示下拉列表。 |
| [hide](dropdown_hide.md) | 因此下拉列表。 |

## 手册
[Dropdown](http://docs.zuoyouxi.com/manual/Sample/Dropdown.html)