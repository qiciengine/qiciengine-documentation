# Tilemap
inherit [qc.Node](CNode.md)

## 描述
瓦片地图，使用Tiled Map Editor制作，Tile Layer Format为CSV，保存为txt文件的地图。
使用时，将txt设置为Tilemap的data后，需要调用[Tilemap.generateLayers()](tilemap_generateLayers.md)来生成[TileLayer](CTileLayer.md)。

## 创建 Tilemap
````
    // 创建一个 Tilemap 节点
    var tilemap  = new qc.game.add.tilemap(parent);
````

## 变量
| 变量名        |  类型     |   作用           |
| ------------- |-------------| -------------|
| nativeSize | qc.Rectangle | 只读，地图的实际大小（不带任何缩放） |
| layers | Array | 图层数组 |
| tilesets | Array | 图集数组 |
| scrollX | number | 水平滚动距离 |
| scrollY | number | 垂直滚动距离 |
| tileWidth | number | 平铺格子的宽度 |
| tileHeight | number | 平铺格子的高度 |
| mapWidth | number | 地图X轴上格子的数量 |
| mapHeight | number | 地图Y轴上格子的数量 |
| data | qc.TextAsset | Tilemap数据 |

## 方法
| 方法名 | 作用 |
| ------------- |-------------|
| [resetNativeSize](tilemap_resetNativeSize.md) | 设置为地图原始的大小 |
| [generateLayers](tilemap_generateLayers.md) | 生成TileLayer |
| [getLayerByIndex](tilemap_getLayerByIndex.md) | 通过序号获取地图层 |
| [getLayerByName](tilemap_getLayerByName.md) | 通过名称获取地图层 |
| [getTilePosition](tilemap_getTilePosition.md) | 获取一个X,Y轴位置在地图中的位置 |

## 参考手册
[瓦片地图](http://docs.zuoyouxi.com/manual/Sample/Tilemap.html)