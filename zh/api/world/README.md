# qc.World
inherit [qc.Node](../gameobject/CNode.md)

## 描述
游戏世界的节点对象，可以使用game.world进行访问。
所有场景中的游戏对象，都是其子孙。

## 变量
| 变量名 | 类型 |作用 |
| ------------- |-------------|-------------|
| centerX | number | 世界的水平中心点 |
| centerY | number | 世界的垂直中心点 |
| pivotX | number | 世界原点的X位置，固定为0 |
| pivotY | number | 世界原点的Y位置，固定为0 |
| bounds | Phaser.Rectangle | 世界的包围盒 |
| camera | Phaser.Camera | 世界相机 |
| width | number | 世界的宽度 |
| height | number | 世界的高度 |

## 事件
| 事件名 | 作用 |
| ------------- |-------------|
| onSizeChange | 大小发生变化的事件 |
