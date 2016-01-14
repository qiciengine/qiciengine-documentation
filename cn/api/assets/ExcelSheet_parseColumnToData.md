# [qc.ExcelSheet](ExcelSheet.md).parseColumnToData

## 原型
* void parseColumnToData(string column)

## 参数说明
| 参数名 | 类型 | 说明 |
| ------------- | ------------- | -------------|
| column | string | 列名 |

## 说明
将一列的数据转化为日期类型。  
由于Excel的日期类型的值为距离1900年1月1日经历的秒数，而javascript中的值为距离1970年1月1日经历的秒数，因此需要进行转换。
