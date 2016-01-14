# 表格数据适配器
## 描述
使用表格来表现的数据集合时，如果数据集合比较大，使用传统的方式，将全部的节点都创建出来，内存开销等都比较大，甚至还有无限数据的展示需求。所以我们将表格的表现和数据分开。  

使用本类来为表格显示视图提供数据和布局等参数信息。使用时，继承该类，并按需求，重载相关函数即可。

## 可重载的函数
| 函数原型 | 描述|
|----------|-----|
|qc.Point getTableSize() | 获取表格的列数和行数，列数和行数中有且仅能有一个为Infinity。 |
|qc.Point findCellWithPos(x, y) | 根据相对于内容区域左上角的偏移值计算出对应的行和列。 |
|qc.Rectangle getCellRect(col, row) | 返回指定列和行的单元格的大小。|
|void revokeCell(cell, col, row) | 当单元格被回收时调用，在此进行单元格的清理操作。|
|void createCell(cell, col, row) | 当单元格创建时调用，在此进行单元格的初始化操作。|

## 固定函数
| 函数原型 | 描述 |
|--------------------|-------|
|void dispatchDataChange() | 通知表格数据发生了变化，在表格对应的数据发生变化时，需要主动调用本函数。|

## 使用方法
定义一个脚本并继承本类
```
var TableData = qc.defineBehaviour('qc.engine.TableData', com.qici.extraUI.TableViewAdapter, function() {
    
}, {
    
});

// 返回表格数据的行数和列数，这里返回一个10列，无限行的表格
TableData.prototype.getTableSize = function() {
	return { x: 10, y: Infinity};
};

// 计算点所在的单元格，这里假设表格由无限个100 * 100紧密连接的单元格组成。
TableData.prototype.findCellWithPos = function(x, y) {
	return { 
		x: Math.floor(x / 100),
		y: Math.floor(y / 100)
	};
};

// 返回单元格的显示位置
TableViewAdapter.prototype.getCellRect = function(col, row) {
	return new qc.Rectangle(col * 100, row * 100, 100, 100);
};

// 回收单元格
TableData.prototype.revokeCell = function(cell, col, row) {
	cell._myTableData = null;
};

// 创建单元格时，为单元格赋予自定义数据
TableData.prototype.createCell = function(cell, col, row) {
	cell._myTableData = 'cell(' + col + ',' + row + ')';
};
```