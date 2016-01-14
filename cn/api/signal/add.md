# [qc.Signal](README.md).add

## 原型
* qc.SignalBinding add(listener:function, listenerContext:object, priority);

## 参数
| 参数名 | 类型 | 说明 |
| ----------- | ----------- | ----------- |
| listener | function | 监听的回调函数 |
| listenerContext | object，undefined | 回调函数的上下文 |
| priority | int | 优先级越高，越早被调用 |
| 返回值 | [qc.SignalBinding](../signalbinding/README.md) | 事件监听器 |


## 说明
添加一个事件监听器
