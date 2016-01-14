# qc.ExcelAsset

## 说明
excel表格数据，具体可参考范例：[Excel配置游戏](http://docs.zuoyouxi.com/manual/Excel/index.html)

## 变量
| 变量名        | 类型 | 作用           |
| ------------- |-------------|-------------|
| key |string | 只读。资源关键字 |
| url |string | 只读。资源的地址 |
| sheetsName | array | 只读。所有的数据表名 |
| sheets | object | 只读。excel表的数据 |
| meta | object | 只读。元数据 |
| uuid | string | 只读。资源的 uuid |

## 方法
| 方法名        | 作用           |
| ------------- |-------------|
| [findSheet](excel_findSheet.md) | 取得某个数据表的信息 |
| [parseToDate](excel_parseToDate.md) | 转换excel的日期数据 |

## 参考手册
[使用Excel](http://docs.zuoyouxi.com/manual/Excel/index.html)
