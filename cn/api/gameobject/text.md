# [qc.GameObjectFactory](GameObjectFactory.md).text

## 原型
* [qc.UIText](CUIText.md) text([qc.Node](CNode.md) parent)

## 参数
| 参数名 | 类型 | 说明 |
| ----------- | ----------- | ----------- |
| parent | [qc.Node](CNode.md) | 挂载的父亲对象（允许为空，空的话挂载到根节点） |

## 描述
创建一个 [qc.UIText](CUIText.md) 文本对象。

## 范例
````
    var text = game.add.text(game.world)
````
