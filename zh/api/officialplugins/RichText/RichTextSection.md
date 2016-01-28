# 富文本显示段

## 描述
用来描述一个富文本的显示结构

## 变量
| 变量名                | 类型                         | 作用            |
| -------------      | -------------              | ------------- |
| lines              | Array                      | 所有的行集合        |
| limitLength        | number                     | 限制的行长度        |
| breakStyle         | number                     | 自动换行的类型       |
| rect               | {x, y, width, height}      | 显示段的范围        |
| margin             | {left, right, top, bottom} | 显示段的外边界       |
| defaultStyle       | RichTextStyle              | 默认的样式         |
| lienSpaces         | Array                      | 行间距           |
| charOrder          | number                     | 文本显示的顺序       |
| chickHandleContext | qc.Node                    | 富文本交互信息的处理对象  |

## 常量
| 常量名                     | 类型            | 作用            |
| -------------           | ------------- | ------------- |
| RichTextSection.LTR_TTB | number        | 文本从左到右，从上到下显示 |
| RichTextSection.LTR_BTT | number        | 文本从左到右，从下到上显示 |
| RichTextSection.RTL_TTB | number        | 文本从右到左，从上到下显示 |
| RichTextSection.RTL_BTT | number        | 文本从右到左，从下到上显示 |
| RichTextSection.TTB_LTR | number        | 文本从上到下，从左到右显示 |
| RichTextSection.TTB_RTL | number        | 文本从上到下，从右到左显示 |
| RichTextSection.BTT_LTR | number        | 文本从下到上，从左到右显示 |
| RichTextSection.BTT_RTL | number        | 文本从下到上，从右到左显示 |


## 方法
| 方法名           | 作用                     |
| ------------- | -------------          |
| reset         | 重置结构为初始状态              |
| closeLastLine | 关闭最后一行                 |
| getLastLine   | 返回最后一行的结构              |
| getLastBlock  | 返回最后一个显示块结构            |
| getCurrLine   | 返回当前可以操作的行             |
| getCurrBlock  | 返回当前可以操作的块             |
| pushStyle     | 设置当前使用的风格              |
| popStyle      | 返回上一个风格，如果没有则返回默认风格    |
| appendElement | 添加一个显示单元               |
| build         | 通过RichTextChunk数组构建显示段 |
| append        | 添加一个富文本结构到显示段          |
| onClick       | 点击显示段，触发交互事件           |
| render        | 绘制显示段                  |

## 参考手册
[RichText](http://docs.zuoyouxi.com/manual/Plugin/RichText.html)