# qc.ExcelSheet

## 说明
excel表格数据，具体可参考范例：[Excel配置游戏](http://docs.zuoyouxi.com/manual/Excel/index.html)

## 变量
| 变量名        | 类型 | 作用           |
| ------------- |-------------|-------------|
| columns |Array | 只读。表的列名数组 |
| rows | Array | 只读。表的行数据 |

## 方法
| 方法名        | 作用           |
| ------------- |-------------|
| [addSortIndex](ExcelSheet_addSortIndex.md) | 为表格数据添加一个排序索引 |
| [addHashIndex](ExcelSheet_addHashIndex.md) | 为表格数据添加一个Hash索引 |
| [getIndex](ExcelSheet_getIndex.md) | 获取一个已经存在的索引 |
| [getPrimary](ExcelSheet_getPrimary.md) | 获取主键排序索引，默认为第一列的排序索引 |
| [find](ExcelSheet_find.md) | 遍历查找满足条件的第一个数据 |
| [findLast](ExcelSheet_findLast.md) | 遍历查找满足条件的最后一个数据 |
| [matches](ExcelSheet_matches.md) | 遍历查找所有满足条件的数据 |
| [parseColumnToData](ExcelSheet_parseColumnToData.md) | 将一列的数据转化为日期类型 |
