# [qc.Node](CNode.md).setAnchor

## 原型
* void setAnchor([qc.Point](../geom/Point.md) min, [qc.Point](../geom/Point.md) max, bool keepRect)

## 参数
| 参数名 | 类型 |  说明 |
| --------- | --------- | --------- |
| min | [qc.Point](../geom/Point.md) | 左上角的基准点，如果为undefined，则认为没有变化 |
| max | [qc.Point](../geom/Point.md) | 右下角的基准点，如果为undefined，则认为没有变化 |
| keepRect | bool | 是否保持当前位置和大小不变，默认为true |

## 描述
设置相对于父亲的锚点。

