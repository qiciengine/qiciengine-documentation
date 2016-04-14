# qc.Node

## 描述
qc.Node 是所有 GameObject 对象的基类，可以挂载各类游戏脚本，本身具有 RectTransform 位置、定位属性，可作为其他节点的父亲、儿子。

## 创建 Node
详见[qc.GameObjectFactory](GameObjectFactory.md)
````
// 创建一个 Node 节点
var node = new qc.game.add.node(parent);
````

## 变量
|   变量名   |   类型    |    作用     |
| ------------- |-------------|-------------|
| uuid | string | 对象的唯一标识符 |
| name | string | 节点的名字 |
| ignoreDestroy | bool | 节点及其孩子在切换场景时不会被析构。__一定要置于根节点才起效__ |
| alpha | number | 透明度值，0 - 1 |
| visible | bool |  是否可见，注意 visible 为 false 时则所有孩子都不显示，visible 为 true 的时则使用孩子们自己的 visible；另外 visiable 为 false 时连 transform 都不再更新计算 |
| parent | [qc.Node](CNode.md) |  父亲节点 |
| worldVisible | bool | 只读，节点最终的 visible |
| mask | PIXI.Graphics | 遮罩，必须为 PIXI.Graphics 对象 |
| children | Array | 只读，儿子列表 |
| colorTint | [qc.Color](../color/README.md) | 混合颜色 |
| scripts | Array | 只读。挂载的逻辑脚本列表 |

### 定位相关
|   变量名   |   类型    |    作用     |
| ------------- |-------------|-------------|
| x | number | 本地 x 坐标（相对于父节点） |
| y | number | 本地 y 坐标（相对于父节点） |
| anchoredX | number | 相对于父亲anchor的X偏移量。UI中大部分使用此属性，而不是x属性。 |
| anchoredY | number | 相对于父亲anchor的Y偏移量。UI中大部分使用此属性，而不是y属性。 |
| scaleX | number | 节点在 X 轴上的缩放 |
| scaleY | number | 节点在 Y 轴上的缩放 |
| pivotX | number | 节点自身的原点X位置（0为左边，1为右边） |
| pivotY | number | 节点自身的原点Y位置（0为上边，1为下边） |
| rotation | number | 旋转角度。在代码中，使用弧度为单位。在编辑器的Inspector面板中，使用角度为单位。 |
| width | number | 节点的宽度 |
| height | number | 节点的高度 |
| minAnchor | [qc.Point](../geom/Point.md) | 只读，定位矩形左上角的坐标（相对于父亲长宽的比例值），请使用方法 [setAnchor](node_setAnchor.md) 进行设置。|
| maxAnchor | [qc.Point](../geom/Point.md) | 只读，定位矩形右下角的坐标（相对于父亲长宽的比例值），请使用方法 [setAnchor](node_setAnchor.md) 进行设置。 |
| left | number | 距离左边的位置（如果minAnchor.x = maxAnchor.x，此时不起效） |
| right | number | 距离右边的位置（如果minAnchor.x = maxAnchor.x，此时不起效） |
| top | number | 距离上边的位置（如果minAnchor.y = maxAnchor.y，此时不起效） |
| bottom | number | 距离下边的位置（如果minAnchor.y = maxAnchor.y，此时不起效） |
| rect | [qc.Rectangle](../geom/Rectangle.md) | 相对父亲节点的矩形包围盒 |
| worldTransform | [qc.Matrix](../geom/Matrix.md) | 在世界中的最终变换矩阵 |
| localBounds | [qc.Rectangle](../geom/Rectangle.md) | 节点自身的显示范围 |
| onRelayout | [qc.Signal](../signal/README.md) | 节点重新布局的事件通知 |

### 交互相关
|   变量名   |   类型    |    作用     |
| ------------- |-------------|-------------|
| interactive | boolean | 节点是否允许交互（即：是否有能力接受输入事件） |
| hitArea | [qc.Rectangle](../geom/Rectangle.md)，[qc.Rectangle](../geom/Ellipse.md)，null，undefined | 碰撞区域 |
| onDown | [qc.Signal](../signal/README.md) | 按下的事件 |
| onUp | [qc.Signal](../signal/README.md) | 松开的事件 |
| onClick | [qc.Signal](../signal/README.md) | 点击的事件 |
| onDragStart | [qc.Signal](../signal/README.md) | 拖拽开始事件 |
| onDrag | [qc.Signal](../signal/README.md) | 拖拽事件，每帧触发 |
| onDragEnd | [qc.Signal](../signal/README.md) | 拖拽结束事件 |
| onDragDrop | [qc.Signal](../signal/README.md) | 拖拽放下事件（目标节点触发） |
| onWheel | [qc.Signal](../signal/README.md) | 滚轮事件 |
| onEnter | [qc.Signal](../signal/README.md) | 光标进入事件 |
| onExit | [qc.Signal](../signal/README.md) | 光标移出事件 |

## 方法
| 方法名 | 作用 |
| ------------- |-------------|
| [addScript](node_addScript.md) | 添加一个逻辑脚本对象（移除请调用 [qc.Behaviour#destroy](../behaviour/destroy.md) 接口） |
| [getScript](node_getScript.md) | 取得一个逻辑脚本对象 |
| [getScripts](node_getScripts.md) | 取得逻辑脚本对象列表 |
| [isDescendantOf](node_isDescendantOf.md) | 判断本对象是否是指定 Node 的子孙节点 |
| [addChild](node_addChild.md) | 添加一个孩子节点到尾部 |
| [addChildAt](node_addChildAt.md) | 添加一个孩子节点到指定位置 |
| [swapChildren](node_swapChildren.md) | 交换两个孩子的位置 |
| [getChildIndex](node_getChildIndex.md) | 取得孩子的位置 |
| [setChildIndex](node_setChildIndex.md) | 设置孩子的位置 |
| [getChildAt](node_getChildAt.md) | 取得指定位置的孩子对象 |
| [removeChild](node_removeChild.md) | 移除一个孩子 |
| [removeChildAt](node_removeChildAt.md) | 在指定的位置删除孩子 |
| [removeChildren](node_removeChildren.md) | 删除所有的孩子 |
| [destroy](node_destroy.md) |  销毁本对象（节点先隐藏掉，下一帧才会真正被清除）  |
| [destroyImmediately](node_destroyImmediately.md) |  立刻销毁本节点（不推荐使用）  |
| [find](node_find.md) |  查找子孙节点，可用 '/' 进行级联查询  |
| [addListener](addListener.md) | 监听事件，在对象析构时会自动移除事件监听 |
| [addListenerOnce](addListenerOnce.md) | 增加一次性事件关注，事件响应一次后自动移除监听 |
| [removeListener](removeListener.md) | 手动移除事件 |
| [snapshotAsAtlas](node_snapshotAsAtlas.md) | 将当前节点进行截屏，得到一个[qc.Atlas](../assets/Atlas.md)对象可用于[qc.UIImage](CUIImage.md)使用 |
| [snapshotAsImage](node_snapshotAsImage.md) | 将当前节点进行截屏，得到一个html的Image对象（可直接添加到div中） |

### 定位相关
| 方法名 | 作用 |
| ------------- |-------------|
| [getWorldPosition](node_getWorldPosition.md) | 获取节点在全局坐标系中的位置 |
| [getWorldScale](node_getWorldScale.md) | 获取节点在全局坐标系中的缩放 |
| [getWorldRotation](node_getWorldRotation.md) | 获取节点在全局坐标系中的旋转弧度 |
| [switchParent](node_switchParent.md) | 切换父节点为指定节点，并保证本节点在世界坐标系中的状态不变 |
| [getWorldCorners](node_getWorldCorners.md) | 获取节点在世界坐标中的四个角 |
| [getWorldBox](node_getWorldBox.md) | 获取节点在世界坐标的包围盒 |
| [getBoxIn](node_getBoxIn.md) | 获取节点在指定节点坐标系中的包围盒 |
| [rectContains](node_rectContains.md) | 判断世界坐标中的某个点是否在矩形框的范围内 |
| [toGlobal](node_toGlobal.md) | 本地坐标转换为全局坐标 |
| [toLocal](node_toLocal.md) | 全局坐标转换为本地坐标 |
| [setAnchor](node_setAnchor.md) | 设置锚点定位范围 |
| [setStretch](node_setStretch.md) | 修改可伸缩参数（上、下、左、右边距） |

## 参考手册
[空节点](http://docs.zuoyouxi.com/manual/Sample/Node.html)