# [qc.Bounds](Bounds.md).getBounds

## Prototype
* [qc.Rectangle](../geom/Rectangle.md) getBounds([qc.Node](../gameobject/CNode.md) node, int sizeProvider, bool force, int deep)

## Parameter
| Parameter | type | Description |
| ------------- | ------------- | -------------|
| node | [qc.Node](../gameobject/CNode.md) | Node object |
| sizeProvider | int | The way for size calculate. There are two values:Bounds.USE_BOUNDS(Use the actual display range as the border)、Bounds.USE_RECTTRANSFORM(Use rectTransform as border, unUnaffected by rotation、scale and so on)  |
| force | bool | Whether refresh immediately |
| deep | int | 0:only self, -1:all child nodes, 2:recursive 2 layer in nodes |

## Description
Get the boundary information of a node in its own coordinate system.


## Example
````
    // the real display boundary is affected by child node's rotation or scale.
    var bound = qc.Bounds.getBounds(node, Bounds.USE_BOUNDS, true, -1);

    // the real display boundary isn't affected by child node's rotation or scale.
    var bound = qc.Bounds.getBounds(node, Bounds.USE_RECTTRANSFORM, true, -1);
````
