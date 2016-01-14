# [qc.Node](CNode.md).getScripts

## 原型
* Array getScripts(string script)

## 参数
| 参数名 | 类型 |  说明 |
| --------- | --------- | --------- |
| script | string | 脚本名 |

## 描述
获取逻辑脚本对象列表，返回值 Array 中的元素类型为 [qc.Behaviour](../behaviour/Behaviour.md)。

## 示例
````
    node.getScripts('qc.TweenPosition');
````
