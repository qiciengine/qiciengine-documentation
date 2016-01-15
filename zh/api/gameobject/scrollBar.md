# [qc.GameObjectFactory](GameObjectFactory.md).scrollBar

## 原型
* [qc.ScrollBar](CScrollBar.md) scrollBar([qc.Node](CNode.md) parent, bool createSliders)

## 参数
| 参数名 | 类型 | 说明 |
| ----------- | ----------- | ----------- |
| parent | [qc.Node](CNode.md) | 挂载的父亲对象（允许为空，空的话挂载到根节点） |
| createSliders | boolean | 是否创建一个显示滑条 |

## 描述
创建一个 [qc.ScrollBar](CScrollBar.md) 滚动条

## 范例
````
    var scrollBar = game.add.scrollBar(game.world, true)
````
