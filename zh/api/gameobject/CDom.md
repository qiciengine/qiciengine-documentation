# qc.Dom
inherit [qc.Node](CNode.md)

## 描述
Dom节点，本质上就是个div。由于不需要每帧进行渲染，非常高效。具体请参看[用户手册](http://docs.zuoyouxi.com/manual/Sample/Dom.html)

## 变量
| 变量名        |   类型       |  作用           |
| ------------- |-------------|-------------|
| div | object  |  对应的div元素 |
| pos | 枚举| 节点的位置，qc.Dom.BACK(背景层); qc.Dom.FRON(顶层) |
| innerHTML | string | 内部的HTML元素，当serializable=false时，本字段不能被序列化 |
| className | string | 使用的样式表  |
| serializable | boolean | innerHTML信息是否需要保存，默认为true  |
| overflow | enum | 对应于style.overflow，可取值：auto、hidden、visible、scroll  |
| zIndex | int | 对应于style.zIndex。不能设置为0（游戏场景），值越大表示在上层 |

## 事件
|   事件名      |     作用       |
| ------------- |-------------|
| onVisibleChange | 父亲或自身的可见属性发生变化了的事件 |

## 参考手册
[Dom节点](http://docs.zuoyouxi.com/manual/Sample/Dom.html)