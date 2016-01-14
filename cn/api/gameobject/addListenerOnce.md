# qc.Node#addListenerOnce

## 原型
* void addListenerOnce([qc.Signal](../signal/README.md)signal, [function]listener, [object]listenerContext, [int]priority);

## 参数说明
| 参数名 | 类型 | 说明 |
| ------------- | ------------- | -------------|
| signal | [qc.Signal](../signal/README.md) | 事件对象 |
| listener | function | 事件关注的回调函数 |
| listenerContext | object | listener函数的属主 |
| priority | int | 监听优先级 |

## 说明
增加一次性事件关注，事件响应一次后自动移除监听。

## 范例
````
    this.addListenerOnce(this.game.input.onKeyDown, function(keycode){
            console.log('key down');
    })
````
