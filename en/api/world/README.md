# qc.World
inherit [qc.Node](../gameobject/CNode.md)

## Description
A game has only one world. The world is an abstract place in which all game objects live.
A world is created the same size as your Stage.

## Variables
| Variable | Type | Description |
| ------------- |-------------|-------------|
| centerX | number | The X position corresponding to the center point of the world. |
| centerY | number | The Y position corresponding to the center point of the world. |
| pivotX | number | alway is 0 |
| pivotY | number | alway is 0 |
| bounds | Phaser.Rectangle | The box of world |
| camera | Phaser.Camera | The world camera |
| width | number | The width of world |
| height | number | The height of world |

## Event
| Event | Description |
| ------------- |-------------|
| onSizeChange | When size change, this event is trigged. |
