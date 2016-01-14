# [qc.GameObjectFactory](GameObjectFactory.md).clone

## Prototype
* [qc.Node](CNode.md) clone([qc.Node](CNode.md) node, [qc.Node](CNode.md) parent)
* [qc.Node](CNode.md) clone([qc.Prefab](../assets/Prefab.md) node, [qc.Node](CNode.md) parent)

## Parameters
| Parameter | Type | Description |
| ----------- | ----------- | ----------- |
| node |  [qc.Node](CNode.md) or [qc.Prefab](../assets/Prefab.md) | The object to clone. |
| parent | [qc.Node](CNode.md) | The parent node. |

## Description
Clones the object original and returns the clone.
This function makes a copy of an object in a similar way to the Duplicate command in the editor.

## Example
````
    game.assets.load('test_prefab', 'Assets/prefabs/bullet.bin', function(asset) {
        // clone this asset
        var o = game.add.clone(asset);
    })
````
