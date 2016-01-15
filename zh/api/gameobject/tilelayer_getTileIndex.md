# [qc.TileLayer](CTileLayer.md).getTileIndex

## 原型
* int getTileIndex(int x, int y)

## 参数
| 参数名 | 类型 |  说明 |
| --------- | --------- | --------- |
| x | int | 在水平方向上的位置 |
| y | int | 在竖直方向上的位置 |

## 描述
获取指定位置的Tile使用的图元序号，返回<=0时，表示当前位置没有设置图元；返回Infinity时，表示当前数据还未加载完成，或者数据缺失。
