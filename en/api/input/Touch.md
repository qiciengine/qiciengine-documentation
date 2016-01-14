# qc.Touch

## Description
This module is responsible for touch event handle. User can use game.input.touch to refer this module.
Common interface have been wrapped in [qc.Input](Input.md).

## Paramters
| Paramter | Type | Description |
| ------------- |-------------|-------------|
| enable | boolean | Whether trigger touch event |
| touchCount | int | Read only. The count of touch pressed |
| touchIds | array | Read only. The ids of touch pressed |

## Event
| Event | Description |
| onTouchStart |When touch start, the event is trigged. Event parameter is (id, worldX, worldY) |
| onTouchEnd | When touch end, the event is trigged. Event parameter is (id, worldX, worldY) |
| onTouchMove | When touch move, the event is trigged. Event parameter is (id, worldX, worldY) |

## Method
| Method | Description |
| ------------- |-------------|
| [isAnyTouch](Touch_isAnyTouch.md) | Check whether any touch is pressed |
| [isAnyTouchStart](Touch_isAnyTouchStart.md) | Check whether any touch is pressed in current frame |
| [isTouchStart](Touch_isTouchStart.md) | Check whether a specified touch start |
| [getTouchById](Touch_getTouchById.md) | Get touch by id |
| [getTouchByDeviceId](Touch_getTouchByDeviceId.md) | Get touch by device id |

## ID
| Constant | Description |
| ------------- |-------------|
| Touch.MAIN |  |
