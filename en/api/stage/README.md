# qc.Stage

## Description
A wrap of Phaser.stage, is a root node for all game elements, is parent node of [game.world](../world/README.md), can use game.stage to refer to.

## Paramters
| Paramter | Type | Description |
| ------------- |-------------|-------------|
| runInBackground | bool | Whether is running in the background |
| backgroundColor | [qc.Color](../color/README.md) | The color of background |
| rect | [qc.Rectangle](../geom/Rectangle.md) | The rectangle bound of stage |
| worldTransform | [qc.Matrix](../geom/Matrix.md) | The world transform of stage |
| x | int | alway is 0 |
| y | int | alway is 0 |
| pivotX | int | alway is 0 |
| pivotY | int | alway is 0  |

## Method
| Method | Description |
| ------------- |-------------|
| [updateTransform](updateTransform.md) | Update transforms of stage |
| [destroy](destroy.md) | Destroy stage |
