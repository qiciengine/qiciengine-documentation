# qc.arcade.RigidBody

## 描述
刚体组件，通过物理模拟决定物体的位置。

## 变量
| 变量名         |   类型      |  作用        |
| ------------- |-------------|-------------|
| mass | number | 刚体的质量，当两个刚体发生碰撞时，质量属性将用来计算碰撞后的速度变化，质量越大碰撞后的速度变化越小 |
| moves | boolean | 物体的位置是否由物理系统决定 |
| immovable | boolean | 刚体是否固定不动（即位置不受其他刚体的影响） |
| collideWorldBounds | boolean | 碰到游戏世界的边界是否反弹 |
| allowRotation | boolean | 是否允许刚体旋转 |
| allowGravity | boolean | 是否允许重力 |
| bounce | [qc.Point](../../geom/Point.md) | 刚体碰撞时的反弹力，x或y值为1表示100%反弹，值为0.5表示50%反弹 |
| velocity | [qc.Point](../../geom/Point.md) | 移动速度 |
| maxVelocity | [qc.Point](../../geom/Point.md) | 最大移动速度 |
| acceleration | [qc.Point](../../geom/Point.md) | 加速度 |
| drag | [qc.Point](../../geom/Point.md) | 空气阻力，当阻力大于0时，在移动的过程中会产生速度衰减 |
| gravity | [qc.Point](../../geom/Point.md) | 重力，需要先将 allowGravity 属性设置为true |
| friction | [qc.Point](../../geom/Point.md) | 摩擦力 |
| angularVelocity | number | 角速度，需要先将 allowRotation 设置为true |
| maxAngular | number | 最大角速度 |
| angularAcceleration | number | 角加速度 |
| angularDrag | number | 角阻力，当角阻力大于0时，在旋转的过程中将会产生角速度衰减 |
| checkCollision | object | 当物体向某个方向移动时，是否检查碰撞 |
| ccdIterations | int | 碰撞检测时的离散点数量（0或-1表示不检测离散点），用于解决由于移动速度过快而产生的穿透问题。注意：此值越大开销越大，但碰撞检测的效果越好 |
| collides | array | 需要进行碰撞检测的元素列表，刚体只会与此列表中的元素进行碰撞检测 |
| overlaps | array | 需要进行重叠检测的元素列表，刚体只会与此列表中的元素进行重叠检测 |


## 方法
| 方法名 | 作用 |
| ------------- |-------------|
| [reset](rigidbody/reset.md) | 重置刚体的数据 |
| [addCollide](rigidbody/addCollide.md) | 添加一个碰撞检测节点 |
| [removeCollide](rigidbody/removeCollide.md) | 删除一个碰撞检测节点 |
| [addOverlap](rigidbody/addOverlap.md) | 添加一个重叠检测节点 |
| [removeOverlap](rigidbody/removeOverlap.md) | 删除一个重叠检测节点 |
| [moveToObject](rigidbody/moveToObject.md) | 按照一定的速度移动到目标位置 |
| [velocityFromAngle](rigidbody/velocityFromAngle.md) | 根据角度和速度，得到水平和垂直方向的速度 |
| [velocityFromRotation](rigidbody/velocityFromRotation.md) | 根据弧度和速度，得到水平和垂直方向的速度 |
| [accelerateToObject](rigidbody/accelerateToObject.md) | 以加速度移动到目标位置 |
| [distanceBetween](rigidbody/distanceBetween.md) | 计算相对于某个物体的距离 |
| [angleBetween](rigidbody/angleBetween.md) | 计算相对于某个物体的夹角（弧度） |

## 参考手册
[RigidBody](http://docs.zuoyouxi.com/manual/Plugin/Arcade.html)