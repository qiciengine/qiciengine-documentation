# [qc.Signal](README.md).add

## Prototype
* qc.SignalBinding add(listener:function, listenerContext:object, priority);

## Parameters
| Parameter | Type | Description |
| ----------- | ----------- | ----------- |
| listener | function | The function to call when this Signal is dispatched. |
| listenerContext | object，undefined | The context under which the listener will be executed (i.e. the object that should represent the `this` variable). |
| priority | int | The priority level of the event listener. Listeners with higher priority will be executed before listeners with lower priority. Listeners with same priority level will be executed at the same order as they were added (default = 0) |
| return | [qc.SignalBinding](../signalbinding/README.md) | An Object representing the binding between the Signal and listener. |


## Description
Add an event listener.
