# [qc.TileLayer](CTileLayer.md).getTileIndex

## Prototype
* int getTileIndex(int x, int y)

## Paramters
| Paramter | Type | Description |
| --------- | --------- | --------- |
| x | int | pos in axis x |
| y | int | pos in axis y |

## Description
Get tile index by pos. When result <= 0, indicates there is no tile; result is Infinity, indicates that data is still loading, or data is missing.
