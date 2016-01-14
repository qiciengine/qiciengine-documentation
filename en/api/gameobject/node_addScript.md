# [qc.Node](CNode.md).addScript

## Prototype
* [qc.Behaviour](../behaviour/Behaviour.md) addScript(string script)

## Parameters
| Parameter | Type |  Description |
| --------- | --------- | --------- |
| script | string | The className of the script. |

## Description
Adds a component class named className to the node.  
Use this function to change behaviour of objects on the fly.  

Be careful, call [qc.Behaviour#destroy](../behaviour/destroy.md) to destroy the component.

## Sample
````
    node.addScript('qc.TweenPosition');
````
