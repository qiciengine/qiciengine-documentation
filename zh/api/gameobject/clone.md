# [qc.GameObjectFactory](GameObjectFactory.md).clone

## 原型
* [qc.Node](CNode.md) clone([qc.Node](CNode.md) node, [qc.Node](CNode.md) parent)
* [qc.Node](CNode.md) clone([qc.Prefab](../assets/Prefab.md) node, [qc.Node](CNode.md) parent)

## 参数
| 参数名 | 类型 | 说明 |
| ----------- | ----------- | ----------- |
| node |  [qc.Node](CNode.md) 或 [qc.Prefab](../assets/Prefab.md) | 创建的目标对象 |
| parent | [qc.Node](CNode.md) | 挂载的父亲对象（允许为空） |

## 描述
克隆一个对象出来，克隆目标可以是当前world下的 [qc.Node](CNode.md) 或者某个[qc.Prefab](../assets/Prefab.md)

## 范例
````
    // 先加载prefab资源，加载完毕后再进行复制
    game.assets.load('test_prefab', 'Assets/prefabs/bullet.bin', function(asset) {
        // 复制此节点出来
        var o = game.add.clone(asset);
    })
````
