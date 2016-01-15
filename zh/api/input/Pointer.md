# qc.Pointer

## 描述
鼠标、触摸等产生点事件

## 变量
| 变量名    | 类型    | 作用           |
| ------------- |-------------|-------------|
| game | [qc.Game](../game/README.md) | 只读。对应的游戏实例 |
| downTime | number | 按键按下的时间，单位：毫秒 |
| id | int | 只读。点事件ID |
| deviceId | int | 只读。按键在系统中的ID |
| x | number | 只读。世界X坐标 |
| y | number | 只读。世界Y坐标 |
| startX | number | 只读。记录事件开始时在world坐标系中的X轴坐标 |
| startY | number | 只读。记录事件开始时在world坐标系中的Y轴坐标 |
| isMouse | boolean | 只读。是否是鼠标产生的点事件 |
| isJustDown | boolean | 只读。是否刚刚按下 |
| isJustUp | boolean | 只读。是否刚刚弹起 | 
| isDown | boolean | 只读。按键是否按下 |
| isDowning | boolean | 只读。是否处于按下过程 |
| isUpping | boolean | 只读。是否处于弹起过程 |
| deltaX | number | 只读。按键最后距离上次处理在x轴上移动的距离 |
| deltaY | number | 只读。按键最后距离上次处理在y轴上移动的距离 |
| distanceX | number | 只读。本次事件期间在x轴上移动的距离 |
| distanceY | number | 只读。本次事件期间在y轴上移动的距离 |
| effect | boolean | 只读。是否是有效的事件 |
| eventId | int | 只读。事件ID，默认返回设备ID |