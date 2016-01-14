# qc.ExcelSheet

## Description
excel table data, specific reference sample：[Using Excel](http://docs.qiciengine.com/manual/Excel/index.html)

## Variables
| Variable Name       | Type   |    Description        |
| ------------- | ------------- | -------------|
| columns |Array | Read Only. Table column array |
| rows | Array | Read Only. Table row array |

## Methods
| Method | Description |
| ------------- |-------------|
| [addSortIndex](ExcelSheet_addSortIndex.md) | Add a sort index to tabular data     |
| [addHashIndex](ExcelSheet_addHashIndex.md) |  Add a hash index to tabular data |
| [getIndex](ExcelSheet_getIndex.md) | Get a existed index |
| [getPrimary](ExcelSheet_getPrimary.md) | Get sort index of primary key, sort index for the firest column by default |
| [find](ExcelSheet_find.md) | Traversal search for the first data that satisfies the condition |
| [findLast](ExcelSheet_findLast.md) | Traversal search for the last data that satisfies the condition |
| [matches](ExcelSheet_matches.md) | Traversal search for all datas that satisfies the condition |
| [parseColumnToData](ExcelSheet_parseColumnToData.md) | transforming a column of data into a date class |
