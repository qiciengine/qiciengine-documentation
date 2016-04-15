# qc.Key

## 描述
用来记录按键事件

## 变量
| 变量名    | 类型    | 作用           |
| ------------- |-------------|-------------|
| game | [qc.Game](../game/README.md) | 只读，游戏实例 |
| keyCode | number | 按键键值, 参见 : [qc.Keyboard](Keyboard.md) |
| isJustDown | boolean | 按键是否是在当前帧被按下 |
| isJustUp | boolean | 按键是否是在当前帧弹起 |
| isDown | boolean | 按键当前是否处于按下状态 |

## 方法
| 方法名 | 作用 |
| ------------- |-------------|
| [setState](Key_setState.md) | 直接修改按键状态 |
| [checkRepeat](Key_checkRepeat.md) | 检车按键的重复点击事件 |
