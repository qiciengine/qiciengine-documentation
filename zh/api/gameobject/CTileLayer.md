# TileLayer
inherit [qc.Node](CNode.md)

## 描述
瓦片地图的地图层，在设置Tilemap的data后，需要调用Tilemap.generateLayers()来生成TileLayer。

## 变量
| 变量名        |  类型     |   作用           |
| ------------- |-------------| -------------|
| tilemap | [qc.Tilemap](CTilemap.md) | 地图层所属的地图 |
| layerIndex | int | 地图层在所属地图中索引 |
| scrollXRatio | number | 地图层水平滚动的速率 |
| scrollYRatio | number | 地图层竖直滚动的速率 |

## 方法
| 方法名 | 作用 |
| ------------- |-------------|
| [getTile](tilelayer_getTile.md) | 获取指定位置的格子信息 |
| [getTileIndex](tilelayer_getTileIndex.md) | 获取指定位置格子使用的图元序号 |

## 参考手册
[瓦片地图](http://docs.zuoyouxi.com/manual/Sample/Tilemap.html)