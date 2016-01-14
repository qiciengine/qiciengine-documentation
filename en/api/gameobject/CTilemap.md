# Tilemap
inherit [qc.Node](CNode.md)

## Description
The tilemap file is made by Tiled Map Editor. Tile Layer Format is csv, saved as .txt file.
After setting tilemap, need to call [Tilemap.generateLayers()](tilemap_generateLayers.md) to generate [TileLayer](CTileLayer.md).

## Create Tilemap
````
    var tilemap  = new qc.game.add.tilemap(parent);
````

## Variables
| Variable Name   |   Type      |  Description        |
| ------------- |-------------| -------------|
| nativeSize | qc.Rectangle | Read only. native size(not scale) |
| layers | Array | The layer array |
| tilesets | Array | The tileset array |
| scrollX | number | The scroll distance in axis x |
| scrollY | number | The scroll distance in axis y |
| tileWidth | number | The width of tile |
| tileHeight | number | The height of tile |
| mapWidth | number | The cell count in axis x |
| mapHeight | number | The cell count in axis y |
| data | qc.TextAsset | Tilemap data |

## Methods
| Method        | Description          |
| ------------- |-------------|
| [resetNativeSize](tilemap_resetNativeSize.md) | Reset size to native size |
| [generateLayers](tilemap_generateLayers.md) | Generate the tile layer |
| [getLayerByIndex](tilemap_getLayerByIndex.md) | Get layer by index |
| [getLayerByName](tilemap_getLayerByName.md) | Get layer by name |
| [getTilePosition](tilemap_getTilePosition.md) | Get tile position |

## Manual
[Tilemap](http://docs.qiciengine.com/manual/Sample/Tilemap.html)