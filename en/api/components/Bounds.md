# qc.Bounds

## Description
Represents an axis aligned bounding box.

## Variables
| Variable Name   |   Type      |  Description        |
| ------------- |-------------|-------------|
| sizeProvider | int | The way for size calculate. There are two values:Bounds.USE_BOUNDS(Use the actual display range as the border)、Bounds.USE_RECTTRANSFORM(Use rectTransform as border, unUnaffected by rotation、scale and so on) |
| marginTop | int | The top margin relative to the parent |
| marginBottom | int | The bottom margin relative to the parent |
| marginLeft | int | The left margin relative to the parent |
| marginRight | int | The right margin relative to the parent |
| paddingTop | int | The top margin relative to the child |
| paddingBottom | int | The bottom margin relative to the child |
| paddingLeft | int | The left margin relative to the child |
| paddingRight | int | The right margin relative to the child |

## Methods
| Method        | Description          |
| ------------- |-------------|
| [qc.Bounds.getBounds](bounds_getBounds.md) | Get the boundary info of a node in its own coordinate system. |
| [qc.Bounds.getBox](bounds_getBox.md) |  Get the boundary info of a node in the specified object's coordinate system |
