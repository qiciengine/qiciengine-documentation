# 富文本显示块

## 描述
富文本显示中最小的单元块

## 变量
| 变量名                | 类型                         | 作用            |
| -------------      | -------------              | ------------- |
| line               | RichTextLine               | 所属的行          |
| isClosed           | boolean                    | 块是否已经关闭       |
| style              | RichTextStyle              | 块使用的显示风格      |
| elements           | Array                      | 块内需要绘制的元素     |
| elementRects       | Array                      | 块的显示范围        |
| type               | number                     | 块的类型，0 为文本结构  |
| isFirstBlockInLine | boolean                    | 是否位于行首        |
| rect               | {x, y, width, height}      | 块显示范围         |
| margin             | {left, right, top, bottom} | 块显示的外边距       |
| elementCount       | number                     | 块内所有显示元素的个数   |

## 方法
| 方法名           | 作用            |
| ------------- | ------------- |
| close         | 关闭块           |
| appendElement | 添加显示元素        |
| relayout      | 重新计算范围信息      |
