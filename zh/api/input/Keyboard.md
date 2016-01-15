# qc.Keyboard

## 描述
键盘的输入控制，可以通过game.input.keyboard访问本实例，常用接口已经在[qc.Input](Input.md)中进行的封装。

## 变量
| 变量名    | 类型    | 作用           |
| ------------- |-------------|-------------|
| repeatInterval | int | 重复按键的间隔时间，单位为毫秒。默认100 |
| enable | boolean | 键盘交互开关，默认为true |
| keyCount | int | 只读。当前按下的按键数量。 |
| keyCodes | array | 只读。当前所有被按下的键值 |

## 事件
| 事件名 | 作用 |
| ------------- |-------------|
| onKeyDown | 某个按键被按下了，事件参数：keyCode |
| onKeyUp| 某个按键被松开了，事件参数：keyCode |
| onKeyRepeat| 重复按键事件，事件参数：keyCode |

## 方法
| 方法名 | 作用 |
| ------------- |-------------|
| [isKeyDown](Keyboard_isKeyDown.md) | 判断某个键是否被按下了 |
| [isAnyKey](Keyboard_isAnyKey.md) | 当前是否有按键处于按下状态 |
| [isAnyKeyDown](Keyboard_isAnyKeyDown.md) | 在当前帧，是否有按键被按下 |

## 按键信息列表
| 宏 | 对应按键 |
| ------------- |-------------|
| Keyboard.A - Keyboard.Z | A键 - Z键 |
| Keyboard.ZERO - Keyboard.NINE | 数字键 |
| Keyboard.NUMPAD_0 - Keyboard.NUMPAD_9 | 小键盘数字键 |
| Keyboard.NUMPAD_MULTIPLY | 小键盘 乘键|
| Keyboard.NUMPAD_ADD | 小键盘 加键|
| Keyboard.NUMPAD_ENTER | 小键盘 回车键|
| Keyboard.NUMPAD_SUBTRACT | 小键盘 减键|
| Keyboard.NUMPAD_DECIMAL | 小键盘 小数点键|
| Keyboard.NUMPAD_DIVIDE | 小键盘 除键|
| Keyboard.F1 - Keyboard.F15 | 功能键 |
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
