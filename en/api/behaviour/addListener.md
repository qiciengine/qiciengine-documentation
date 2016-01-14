# qc.Behaviour#addListener

## Prototype
* void addListener([qc.Signal](../signal/README.md)signal, [function]listener, [object]listenerContext, [int]priority);

## Paramters
| Paramter | Type | Description |
| ------------- | ------------- | -------------|
| signal | [qc.Signal](../signal/README.md) | Event signal object |
| listener | function | event callback |
| listenerContext | object | owner of listener |
| priority | int | priority of listener |

## Description
Listen event hook, it will be removed automatically when object destroy.

## Example
````
    this.addListener(this.game.input.onKeyDown, function(keycode){
            console.log('key down');
    })
````
