# [qc.Node](CNode.md).switchParent

## 原型
void switchParent([qc.Node](CNode.md) parent, int index)

## 参数
| 参数名 | 类型 |  说明 |
| --------- | --------- | --------- |
| parent | [qc.Node](CNode.md) | 要切换的父亲节点 |
| index | int | 期望添加的位置 |

## 描述
切换父节点为指定节点，节点挂载在新父亲的 index 位置，并保证本节点在世界坐标系中的状态不变。

