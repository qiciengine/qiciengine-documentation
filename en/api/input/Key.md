# qc.Key

## Description
Used for record information of key event.

## Paramters
| Paramter | Type | Description |
| ------------- |-------------|-------------|
| game | [qc.Game](../game/README.md) | Read only. game instance |
| keyCode | number | Key code, see : [qc.Keyboard](Keyboard.md) |
| isJustDown | boolean | Whether key is pressed in current frame |
| isJuseUp | boolean | Whether key pop up in current frame |
| isDown | boolean | Whether key is pressed |

## Method
| Method | Description |
| ------------- |-------------|
| [setState](Key_setState.md) | Set the state of key directly |
| [checkRepeat](Key_checkRepeat.md) | Check whether key is pressed repeatly |
