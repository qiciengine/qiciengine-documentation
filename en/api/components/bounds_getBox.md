# [qc.Bounds](Bounds.md).getBox

## Prototype
* [qc.Rectangle](../geom/Rectangle.md) getBox([qc.Node](../gameobject/CNode.md) node, int sizeProvider, bool force, int deep, [qc.Node](../gameobject/CNode.md) target)

## Parameter
| Parameter | type | Description |
| ------------- | ------------- | -------------|
| node | [qc.Node](../gameobject/CNode.md) | Node object |
| sizeProvider | int | The way for size calculate. There are two values:Bounds.USE_BOUNDS(Use the actual display range as the border)、Bounds.USE_RECTTRANSFORM(Use rectTransform as border, unUnaffected by rotation、scale and so on)  |
| force | bool | Whether refresh immediately |
| deep | int | 0:only self, -1:all child nodes, 2:recursive 2 layer in nodes |
| target | [qc.Node](../gameobject/CNode.md) | target node |

## Description
Get the boundary info of a node in the specified object's coordinate system

## Example
````
    // the real display boundary is affected by child node's rotation or scale in the world coordinate system.
    var bound = qc.Bounds.getBox(node, Bounds.USE_BOUNDS, true, -1, game.world);

    // the real display boundary isn't affected by child node's rotation or scale in the world coordinate system.
    var bound = qc.Bounds.getBox(node, Bounds.USE_RECTTRANSFORM, true, -1, game.world);
````
