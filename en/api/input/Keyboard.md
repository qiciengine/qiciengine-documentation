# qc.Keyboard

## Description
This module is responsible for keyboard event handle. User can use game.input.keyboard to refer this module.
Common interface have been wrapped in [qc.Input](Input.md).

## Paramters
| Paramter | Type | Description |
| ------------- |-------------|-------------|
| repeatInterval | int | Interval time for checking repeat hit, 100ms by default |
| enable | boolean | Whether trigger keyboard event |
| keyCount | int | Read only. The count of key pressed |
| keyCodes | array | Read only. The ids of key pressed |

## Event
| Event | Description |
| ------------- |-------------|
| onKeyDown | When key is pressed, the event is trigged. Event parameter is keyCode |
| onKeyUp| When key pop up, the event is trigged. Event parameter is keyCode |
| onKeyRepeat| When key keep pressed, the event is trigged. Event parameter is keyCode |

## Method
| Method | Description |
| ------------- |-------------|
| [isKeyDown](Keyboard_isKeyDown.md) | Check whether a speicified key is pressed |
| [isAnyKey](Keyboard_isAnyKey.md) | Check whether any key is pressed |
| [isAnyKeyDown](Keyboard_isAnyKeyDown.md) | Check whether any key is pressed in current frame |

## Key
| Constant | Description |
| ------------- |-------------|
| Keyboard.A - Keyboard.Z |  |
| Keyboard.ZERO - Keyboard.NINE |  |
| Keyboard.NUMPAD_0 - Keyboard.NUMPAD_9 |  |
| Keyboard.NUMPAD_MULTIPLY | |
| Keyboard.NUMPAD_ADD | |
| Keyboard.NUMPAD_ENTER | |
| Keyboard.NUMPAD_SUBTRACT | |
| Keyboard.NUMPAD_DECIMAL | |
| Keyboard.NUMPAD_DIVIDE | |
| Keyboard.F1 - Keyboard.F15 |  |
| Keyboard.COLON | |
| Keyboard.EQUALS | |
| Keyboard.UNDERSCORE | |
| Keyboard.QUESTION_MARK | |
| Keyboard.TILDE | |
| Keyboard.OPEN_BRACKET | |
| Keyboard.BACKWARD_SLASH | |
| Keyboard.CLOSED_BRACKET | |
| Keyboard.QUOTES | |
| Keyboard.BACKSPACE | |
| Keyboard.TAB | |
| Keyboard.CLEAR | |
| Keyboard.ENTER | |
| Keyboard.SHIFT | |
| Keyboard.CONTROL | |
| Keyboard.ALT | |
| Keyboard.META | |
| Keyboard.META_RWIN | |
| Keyboard.META_RMAC | |
| Keyboard.CAPS_LOCK | |
| Keyboard.ESC | |
| Keyboard.SPACEBAR | |
| Keyboard.PAGE_UP | |
| Keyboard.PAGE_DOWN | |
| Keyboard.END | |
| Keyboard.HOME | |
| Keyboard.LEFT | |
| Keyboard.UP | |
| Keyboard.RIGHT | |
| Keyboard.DOWN | |
| Keyboard.INSERT | |
| Keyboard.DELETE | |
| Keyboard.HELP | |
| Keyboard.NUM_LOCK | |
| Keyboard.PLUS | |
| Keyboard.MINUS | |
