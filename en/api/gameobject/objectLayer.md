# [qc.GameObjectFactory](GameObjectFactory.md).objectLayer

## Prototype
* [qc.ObjectLayer](CObjectLayer.md) objectLayer([qc.Node](CNode.md) parent);

## Paramters
| Paramter | Type | Description |
| ----------- | ----------- | ----------- |
| parent | [qc.Node](CNode.md) | Optional node to add the object to. If not specified it will be added to the World. |

## Description
Creaet a [qc.ObjectLayer](CObjectLayer.md).

## Example
````
    var objectLayer = game.add.objectLayer(game.world)
````
