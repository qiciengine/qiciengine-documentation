# qc.Node#addListener

## Prototype
* void addListenerOnce([qc.Signal](../signal/README.md)signal, [function]listener, [object]listenerContext, [int]priority);

## Paramters
| Paramter | Type | Description |
| ------------- | ------------- | -------------|
| signal | [qc.Signal](../signal/README.md) | Event signal object |
| listener | function | event callback |
| listenerContext | object | owner of listener |
| priority | int | priority of listener |

## Description
Listen event hook once, it will be removed automatically when event trigged once.

## Example
````
    this.addListenerOnce(this.game.input.onKeyDown, function(keycode){
            console.log('key down');
    })
````
