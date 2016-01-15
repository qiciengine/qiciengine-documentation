# [qc.Node](CNode.md).addScript

## 原型
* [qc.Behaviour](../behaviour/Behaviour.md) addScript(string script)

## 参数
| 参数名 | 类型 |  说明 |
| --------- | --------- | --------- |
| script | string | 脚本名 |

## 描述
添加一个逻辑脚本对象。

注意，移除脚本通过 [qc.Behaviour#destroy](../behaviour/destroy.md) 接口来完成。

## 示例
````
    node.addScript('qc.TweenPosition');
````
