# [qc.Node](CNode.md).getWorldRotation

## Prototype
* [qc.Point](../geom/Point.md) getWorldRotation(void)

## Description
Get the world rotation of node.

If skew in axis x is not same as skew in axis y, return 0. Then you should call [qc.Node#getWorldSkew](node_getWorldSkew.md) to get skew. Rotation and skew property can only have a valid value.
