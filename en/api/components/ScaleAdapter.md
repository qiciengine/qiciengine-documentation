# qc.ScaleAdapter

## Description
Adaptive resolution component.

## Variables
| Variable Name   |   Type      |  Description        |
| ------------- |-------------|-------------|
| target | [qc.Node](../gameobject/CNode.md)  |  target object |
| referenceResolution | qc.Point | Reference resolution  |
| manualType | int | Scale type. see[Constant](#_3) |
| fullTarget | boolean | Whether to fill full area |

## Constant
| Constant         |   Value      |  Description        |
| ------------- |-------------|-------------|
| ScaleAdapter.NONE | 0 | Not scale |
| ScaleAdapter.MANUAL_HEIGHT | 1 | Scale base on height. the height of area is referenceResolution.y |
| ScaleAdapter.MANUAL_WIDTH | 2 |  Scale base on width. the height of area is referenceResolution.x |
| ScaleAdapter.EXPAND | 3 | Scale to make it exactly place in the target area |
| ScaleAdapter.SHRIKN | 4 | Scale to make it surround the target area |
| ScaleAdapter.FILL | 5 | Scale width and height individually, make target resolution is equal to referenceResolution |

## Manual
[AdapterResolution](http://docs.qiciengine.com/manual/UI/AdapterResolution.html)