# [qc.ExcelSheet](ExcelSheet.md).addHashIndex

## Prototype
* [qc.ExcelHashSheetIndex](ExcelHashSheetIndex.md) addHashIndex(name:string, columnName:string, unique:boolean)

## Parameter
| Parameter | type | Description |
| ------------- | ------------- | -------------|
| name | string | Alias name of index |
| columnName | string | Alias name of hash key |
| unique | boolean | Check if the key is the only |

## Description
Use the specified column name to create a hash index, after creation, data can be obtained directly by value.
