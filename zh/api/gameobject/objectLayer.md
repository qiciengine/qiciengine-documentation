# [qc.GameObjectFactory](GameObjectFactory.md).objectLayer

## 原型
* [qc.ObjectLayer](CObjectLayer.md) objectLayer([qc.Node](CNode.md) parent);

## 参数说明
| 参数名 | 类型 | 说明 |
| ------------- | ------------- | -------------|
| parent | [qc.Node](CNode.md) | 挂载的父亲对象（允许为空，空的话挂载到根节点）

## 说明
创建一个[qc.ObjectLayer](CObjectLayer.md)瓦片地图对象层

## 范例
````
    var objectLayer = game.add.objectLayer(game.world)
````
