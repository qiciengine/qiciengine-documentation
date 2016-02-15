# [qc.Dropdown](CDropdown.md)#addOptions

## 原型
* void addOptions(Array options)

## 参数说明
| 参数名称 | 类型 | 描述 |
| --------- | --------- | --------- |
| options | Array |  待添加的选项列表，选项可以是字符串，也可以是图片。 |

## 描述
添加多个选项到下拉框。

## 范例
````
	// 添加2个文本选项
    dropdown.addOptions(['Option A', 'Option B']);

    // 添加一个图片选项
    dropdown.addOptions([game.assets.find('icon')]);
````
