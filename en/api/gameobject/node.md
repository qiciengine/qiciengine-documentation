# [qc.GameObjectFactory](GameObjectFactory.md).node

## Prototype
* [qc.Node](CNode.md) node([qc.Node](CNode.md) parent)

## Parameters
| Paramter | Type | Description |
| ----------- | ----------- | ----------- |
| parent | [qc.Node](CNode.md) |  Optional node to add the object to. If not specified it will be added to the World. |

## Description
Create a [`Node`](CNode.md).

## Example
````
    var node = game.add.node(game.world)
````
