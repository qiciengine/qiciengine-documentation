# [qc.TableLayout](TableLayout.md).getCellStyle

## 原型
* object getCellStyle(int column, int row)

## 参数说明
| 参数名 | 类型 | 说明 |
| ------------- | ------------- | -------------|
| column | int | 列 |
| row | int | 行 |

## 说明
得到一个单元格的样式。
当获取样式时，对于每个细节参数（水平对齐方式，垂直对齐方式，上、右、下、左边距）优先返回本单元格设置的样式，如果没有单独设置，则返回行或者列中较晚设置的样式

## 范例
返回的 style 格式如下：
````
    {
        align : 0,
        timestamp : 0,
        paddingLeft : NaN,
        paddingRight : NaN,
        paddingTop : NaN,
        paddingBottom : NaN,
        cellWidth : NaN,
        cellHeight : NaN
    };
````
