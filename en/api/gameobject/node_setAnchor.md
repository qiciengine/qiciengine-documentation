# [qc.Node](CNode.md).setAnchor

## Prototype
* void setAnchor([qc.Point](../geom/Point.md) min, [qc.Point](../geom/Point.md) max, bool keepRect)

## Parameters
| Parameter | Type | Description |
| --------- | --------- | --------- |
| min | [qc.Point](../geom/Point.md) | Set up minAnchor. if undefined, minAnchor is no change. |
| max | [qc.Point](../geom/Point.md) | Set up maxAnchor. if undefined, maxAnchor is no change. |
| keepRect | bool | Default true. Keep the current position and size unchanged. |

## Description
Set the distance of this rectangle relative to a specified edge of the parent rectangle, while also setting its size.

