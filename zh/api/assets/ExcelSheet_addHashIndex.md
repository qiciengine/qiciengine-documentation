# 
# [qc.ExcelSheet](ExcelSheet.md).addHashIndex

## 原型
* [qc.ExcelHashSheetIndex](ExcelHashSheetIndex.md) addHashIndex(name:string, columnName:string, unique:boolean)

## 参数说明
| 参数名 | 类型 | 说明 |
| ------------- | ------------- | -------------|
| name | string | 索引的别名 |
| columnName | string | 作为hash键值的别名 |
| unique | boolean | 键值是否唯一 |

## 说明
使用指定列名创建一个hash索引，创建后，可以直接通过值获取数据
