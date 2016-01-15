# [qc.Bounds](Bounds.md).getBounds

## 原型
* [qc.Rectangle](../geom/Rectangle.md) getBounds([qc.Node](../gameobject/CNode.md) node, int sizeProvider, bool force, int deep)

## 参数说明
| 参数名 | 类型 | 说明 |
| ------------- | ------------- | -------------|
| node | [qc.Node](../gameobject/CNode.md) | Node 节点 |
| sizeProvider | int | 取边框的方式，有两个取值：Bounds.USE_BOUNDS(使用实际显示范围作为边框)、Bounds.USE_RECTTRANSFORM(使用 rectTransform 作为边框，不受旋转缩放的影响) |
| force | bool | 是否立即刷新边框 |
| deep | int | 0不计算子节点，-1计算所有子节点，2计算2层子节点 |

## 说明
获取一个节点在自身坐标系下的边界信息

## 范例
````
    // 子节点旋转缩放的实际显示范围影响返回的边界信息
    var bound = qc.Bounds.getBounds(node, Bounds.USE_BOUNDS, true, -1);

    // 子节点旋转缩放的实际显示范围不影响返回的边界信息
    var bound = qc.Bounds.getBounds(node, Bounds.USE_RECTTRANSFORM, true, -1);
````
