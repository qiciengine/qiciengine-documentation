# qc.Bounds

## 描述
为节点提供边界信息查询和编辑功能

## 属性
| 变量名         |   类型      |  作用        |
| ------------- |-------------|-------------|
| sizeProvider | int | 尺寸提供方式，有两个取值：Bounds.USE_BOUNDS(使用实际显示范围作为边框)、Bounds.USE_RECTTRANSFORM(使用 rectTransform 作为边框，不受旋转缩放的影响) |
| marginTop | int | 相对父节点的上边边距 |
| marginBottom | int | 相对父节点的下边边距 |
| marginLeft | int | 相对父节点的左边边距 |
| marginRight | int | 相对父节点的右边边距 |
| paddingTop | int | 相对子节点的上边边距 |
| paddingBottom | int | 相对子节点的下边边距 |
| paddingLeft | int | 相对子节点的左边边距 |
| paddingRight | int | 相对子节点的右边边距 |

## 方法
| 方法名     |  作用        |
| ------------- |-------------|
| [qc.Bounds.getBounds](bounds_getBounds.md) | 获取一个节点在自身坐标系下的边界信息（可指定不同的sizeProvider） |
| [qc.Bounds.getBox](bounds_getBox.md) | 获取一个节点在指定对象坐标系中的边界信息（可指定不同的sizeProvider） |
