# qc.Pointer

## Description
The class contains information about point event by mouse and touch trigged.

## Paramters
| Paramter | Type | Description |
| ------------- |-------------|-------------|
| game | [qc.Game](../game/README.md) | Read only. game instance |
| downTime | number | The press time, unit: ms|
| id | int | Read only. ID  of pointer |
| deviceId | int | Read only. device id |
| x | number | Read only. x value in world coordinate |
| y | number | Read only. y value in world coordinate |
| startX | number | Read only. x value in world coordinate when event start |
| startY | number | Read only. y value in world coordinate when event start |
| isMouse | boolean |  Read only. when event is trigged by mouse, it is true |
| isJustDown | boolean | Read only. Whether is just down  |
| isJustUp | boolean |Read only. Whether just up |
| isDown | boolean | Read only. Whether is down|
| isDowning | boolean | Read only. Whether is downing |
| isUpping | boolean | Read only. Whether is uping |
| deltaX | number | Read only. Delta moved distance in axis x |
| deltaY | number | Read only. Delta moved distance in axis y |
| distanceX | number | Read only. Total moved distance in axis x |
| distanceY | number | Read only. Total moved distance in axis y|
| effect | boolean | Read only. Whether is a effect event |
| eventId | int | Read only.  Event id, device id by default |
