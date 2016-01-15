# [qc.GameObjectFactory](GameObjectFactory.md).tilemap

## 原型
* [qc.Tilemap](CTilemap.md) tilemap([qc.Node](CNode.md) parent);

## 参数说明
| 参数名 | 类型 | 说明 |
| ------------- | ------------- | -------------|
| parent | [qc.Node](CNode.md) | 挂载的父亲对象（允许为空，空的话挂载到根节点）|

## 说明
创建一个[qc.Tilemap](CTilemap.md)瓦片地图

## 范例
````
    var tilemap = game.add.tilemap(game.world)
````
