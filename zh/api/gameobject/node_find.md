# [qc.Node](CNode.md).find

## 原型
* [qc.Node](CNode.md) find(string path)

## 参数
| 参数名 | 类型 |  说明 |
| --------- | --------- | --------- |
| path | string | 查找的路径，允许使用 '/' 来进行级联 |

## 描述
查找子孙节点。

## 示例
````
    node.find('uiLogin/loginBtn/text');
````
