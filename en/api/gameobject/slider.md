# [qc.GameObjectFactory](GameObjectFactory.md).slider

## Prototype
* [qc.Slider](CSlider.md) slider([qc.Node](CNode.md) parent)

## Paramters
| Paramter | Type | Description |
| ----------- | ----------- | ----------- |
| parent | [qc.Node](CNode.md) | Optional node to add the object to. If not specified it will be added to the World. |
| createSliders | boolean |  Whether to create a slider |

## Description
Creaet a [qc.Slider](CSlider.md).

## Example
````
    var slider = game.add.slider(game.world, true)
````
