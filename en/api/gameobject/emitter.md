# [qc.GameObjectFactory](GameObjectFactory.md).emitter

## Prototype
* [qc.Emitter](CEmitter.md) emitter([qc.Node](CNode.md) parent);

## Parameters
| Paramter | Type | Description |
| ----------- | ----------- | ----------- |
| parent | [qc.Node](CNode.md) |  Optional node to add the object to. If not specified it will be added to the World. |

## Description
Create a [qc.Emitter](CEmitter.md).

## Example
````
    var emitter = game.add.emitter(game.world)
````
