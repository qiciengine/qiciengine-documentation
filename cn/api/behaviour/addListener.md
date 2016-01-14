# qc.Behaviour#addListener

## 原型
* void addListener([qc.Signal](../signal/README.md)signal, [function]listener, [object]listenerContext, [int]priority);

## 参数说明
| 参数名 | 类型 | 说明 |
| ------------- | ------------- | -------------|
| signal | [qc.Signal](../signal/README.md) | 事件对象 |
| listener | function | 事件关注的回调函数 |
| listenerContext | object | listener函数的属主 |
| priority | int | 监听优先级 |

## 说明
监听事件，在 [qc.Behaviour]组件对象析构时，会自行对事件进行移除操作，不需要手动调用移除事件的操作

## 范例
````
    this.addListener(this.game.input.onKeyDown, function(keycode){
            console.log('key down');
    })
````
