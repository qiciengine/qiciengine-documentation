# [qc.Signal](README.md).addOnce

## 原型
* qc.SignalBinding addOnce(listener:function, listenerContext:object, priority);

## 参数
| 参数名 | 类型 | 说明 |
| ----------- | ----------- | ----------- |
| listener | function | 监听的回调函数 |
| listenerContext | object，undefined | 回调函数的上下文 |
| priority | int | 优先级越高，越早被调用 |

## 说明
添加一个事件监听器，触发后自动被移除
