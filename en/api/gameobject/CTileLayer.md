# TileLayer
inherit [qc.Node](CNode.md)

## Description
The tile layer of tile map. After setting tilemap, need to call Tilemap.generateLayers() to generate the tile layer.

## Variables
| Variable Name   |   Type      |  Description        |
| ------------- |-------------| -------------|
| tilemap | [qc.Tilemap](CTilemap.md) | tile map |
| layerIndex | int | The layer index of tile layer |
| scrollXRatio | number | Scroll ratio in axis x. |
| scrollYRatio | number | Scroll ratio in axis y. |

## Methods
| Method        | Description          |
| ------------- |-------------|
| [getTile](tilelayer_getTile.md) | Get tile information |
| [getTileIndex](tilelayer_getTileIndex.md) | Get tile index |

## Manual
[Tilemap](http://docs.qiciengine.com/manual/Sample/Tilemap.html)