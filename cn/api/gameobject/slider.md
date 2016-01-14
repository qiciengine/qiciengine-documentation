# [qc.GameObjectFactory](GameObjectFactory.md).slider

## 原型
* [qc.Slider](CSlider.md) slider([qc.Node](CNode.md) parent, boolean createSliders)

## 参数
| 参数名 | 类型 | 说明 |
| ----------- | ----------- | ----------- |
| parent | [qc.Node](CNode.md) | 挂载的父亲对象（允许为空，空的话挂载到根节点） |
| createSliders | boolean |  是否创建一个显示滑条 |

## 描述
创建一个 [qc.Slider](CSlider.md) 滑条

## 范例
````
    var slider = game.add.slider(game.world, true)
````
