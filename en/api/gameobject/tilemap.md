# [qc.GameObjectFactory](GameObjectFactory.md).tilemap

## Prototype
* [qc.Tilemap](CTilemap.md) tilemap([qc.Node](CNode.md) parent);

## Paramters
| Paramter | Type | Description |
| ----------- | ----------- | ----------- |
| parent | [qc.Node](CNode.md) | Optional node to add the object to. If not specified it will be added to the World. |

## Description
Create a [qc.Tilemap](CTilemap.md).

## Example
````
    var tilemap = game.add.tilemap(game.world)
````
