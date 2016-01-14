# [qc.TableLayout](TableLayout.md).getCellRect

## 原型
* [qc.Rectangle](../geom/Rectangle.md) getCellRect(node, force)

## 参数说明
| 参数名 | 类型 | 说明 |
| ------------- | ------------- | -------------|
| node | [qc.Node](../gameobject/CNode.md) | 节点 |
| force | bool | 是否强制重新计算 |

## 说明
获取表格单元格的包围大小，对于已经设置了尺寸提供器的节点使用节点设置，否则使用表格的优先设置
