# [qc.Node](CNode.md).getWorldRotation

## 原型
* [qc.Point](../geom/Point.md) getWorldRotation(void)

## 描述
获取节点在全局坐标系中的旋转弧度。

如果x,y轴的斜拉角度不一致，则得到的旋转为 Skew，返回 0，这时候可以通过 [qc.Node#getWorldSkew](node_getWorldSkew.md) 来获取。
Rotation和Skew只能有一个存在有效值。
