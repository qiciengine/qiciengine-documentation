# qc.Mouse

## Description
This module is responsible for mouse event handle. User can use game.input.mouse to refer this module.
Common interface have been wrapped in [qc.Input](Input.md).

## Paramters
| Paramter | Type | Description |
| ------------- |-------------|-------------|
| enable | boolean | Whether trigger mouse event|
| mouseWheel | object | Delta distance that mouse scroll in two frame, value like {deltaX: number, deltaY: number} |
| mouseCount | int | The count of mouse pressed |
| mouseIds | array | All ids of mouse pressed |

## Event
| Event | Description |
| ------------- |-------------|
| onMouseDown | When mouse is pressed, this event is trigged, Event parameter is (button, worldX, worldY) |
| onMouseUp | When mouse pop up, this event is trigged, Event parameter is (button, worldX, worldY) |
| onMouseMove | When mouse move, this event is trigged, Event parameter is (button, worldX, worldY) |
| onMousePressMove |  When mouse is pressed and moved, this event is trigged, Event parameter is (button, worldX, worldY)  |
| onMouseWheel |  When mouse wheel scroll, this event is trigged, Event parameter is (wheelDelta, wheelDeltaX, wheelDeltaY) |

## Method
| Method | Description |
| ------------- |-------------|
| [isAnyMouse](Mouse_isAnyMouse.md) | Check whether any mouse is pressed |
| [isAnyMouseDown](Mouse_isAnyMouseDown.md) | Check whether any mouse is pressed in current frame |
| [isMouseDown](Mouse_isMouseDown.md) | Check whether a specified key is pressed |
| [getMouseById](Mouse_getMouseById.md) | Get mouse by id |

## Mouse ID
| Constant | Description |
| ------------- |-------------|
| Mouse.NONE |  |
| Mouse.BUTTON_LEFT |  |
| Mouse.BUTTON_MIDDLE |  |
| Mouse.BUTTON_RIGHT |  |
| Mouse.BUTTON_BACK |  |
| Mouse.BUTTON_FORWORD |  |
