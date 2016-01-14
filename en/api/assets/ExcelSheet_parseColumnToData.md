# [qc.ExcelSheet](ExcelSheet.md).parseColumnToData

## Prototype
* void parseColumnToData(string column)

## Parameter
| Parameter | type | Description |
| ------------- | ------------- | -------------|
| column | string | Column name |

## Description
Translate a column of data into a date type.
Because the value of the date type of Excel is the number of seconds that has experienced in January 1, 1900, while the value of JavaScript is the number of seconds that has experienced in January 1, 1970, it needs to be converted.
