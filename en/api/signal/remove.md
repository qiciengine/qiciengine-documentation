# [qc.Signal](README.md).remove

## Prototype
* void remove(listener:function, listenerContext:object);

## Parameters
| Parameter | Type | Description |
| ----------- | ----------- | ----------- |
| listener | function | Handler function that should be removed. |
| listenerContext | object，undefined | Execution context (since you can add the same handler multiple times if executing in a different context). |

## Description
Remove a single event listener.
