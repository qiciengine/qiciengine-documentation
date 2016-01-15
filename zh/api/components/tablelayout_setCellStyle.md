# [qc.TableLayout](TableLayout.md).setCellStyle

## 原型
* void setCellStyle(int column, int row, int align, int paddingTop, int paddingRight, int paddingBottom, int paddingLeft, int cellWidth, int cellHeight)

## 参数说明
| 参数名 | 类型 | 说明 |
| ------------- | ------------- | -------------|
| column | int | 列 |
| row | int | 行 |
| align | int | 布局对齐方式  |
| paddingTop、paddingRight、paddingBottom、paddingLeft | int | 单元格内边框的上、右、底、左边距 |
| cellWidth | int | 单元格宽 |
| cellHeight | int | 单元格高 |

## 说明
设置一个单元格样式。
当获取样式时，对于每个细节参数（水平对齐方式，垂直对齐方式，上、右、下、左边距）优先返回本单元格设置的样式，如果没有单独设置，则返回行或者列中较晚设置的样式
