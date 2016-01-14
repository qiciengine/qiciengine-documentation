# [qc.GameObjectFactory](GameObjectFactory.md).progressBar

## Prototype
[qc.ProgressBar](CProgressBar.md) progressBar([qc.Node](CNode.md) parent)

## Paramters
| Paramter | Type | Description |
| ----------- | ----------- | ----------- |
| parent | [qc.Node](CNode.md) | Optional node to add the object to. If not specified it will be added to the World. |
| createSliders | boolean |  Whether to create a slider |

## Description
Creaet a [qc.ProgressBar](CProgressBar.md).

## Example
````
    var progressBar = game.add.progressBar(game.world, true)
````
