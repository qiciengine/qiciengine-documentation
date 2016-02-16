# [qc.GameObjectFactory](GameObjectFactory.md).scrollBar

## Prototype
* [qc.ScrollBar](CScrollBar.md) scrollBar([qc.Node](CNode.md) parent, bool createSliders)

## Paramters
| Paramter | Type | Description |
| ----------- | ----------- | ----------- |
| parent | [qc.Node](CNode.md) | Optional node to add the object to. If not specified it will be added to the World. |
| createSliders | boolean | Whether to create a slider |

## Description
Create a [qc.ScrollBar](CScrollBar.md).

## Example
````
    var scrollBar = game.add.scrollBar(game.world, true)
````
