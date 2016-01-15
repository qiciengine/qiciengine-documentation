# [qc.GameObjectFactory](GameObjectFactory.md).progressBar

## 原型
[qc.ProgressBar](CProgressBar.md) progressBar([qc.Node](CNode.md) parent, boolean createSliders)

## 参数
| 参数名 | 类型 | 说明 |
| ----------- | ----------- | ----------- |
| parent | [qc.Node](CNode.md) | 挂载的父亲对象（允许为空，空的话挂载到根节点） |
| createSliders | boolean |  是否创建一个显示滑条 |

## 描述
创建一个 [qc.ProgressBar](CProgressBar.md) 进度条

## 范例
````
    var progressBar = game.add.progressBar(game.world, true)
````
