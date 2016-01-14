# qc.Prefab

## Description
Prefabricated resources. In the scene editor it will automatically create prefabricated resource when object is dragged into the specified directory of project. The prefabricated resource save the information of the object. When load this prefab resource, the qc.Prefab object is automatically created. Also we can clone many this prefab objects throught  [game.add.clone](../gameobject/clone.md)

## Variables
| Variable Name        | Type | Description           |
| ------------- |-------------|-------------|
| uuid | string | Read Only. the unique id of resource|
| dependences | Array | Read Only. The dependent resource list of prefab |

## Methods
| Method        | Description          |
| ------------- |-------------|
| [hasUnloadedDependence](Prefab_hasUnloadedDependence.md) | Whether there is a dependency on the resource not loaded successfully |

## Manual
[Prefab](http://docs.qiciengine.com/manual/Prefab/index.html)