# qc.Touch

## 描述
触摸板的输入控制。可以通过game.input.touch访问本实例，常用接口已经在[qc.Input](Input.md)中进行的封装，请优先使用。

## 变量
| 变量名    | 类型    | 作用           |
| ------------- |-------------|-------------|
| enable | boolean | 触摸交互开关，默认为true |
| touchCount | int | 当前触摸点的数量 |
| touchIds | array | 当前所有触摸事件id |

## 事件
| 事件名 | 作用 |
| ------------- |-------------|
| onTouchStart | 触摸开始事件，参数：id, worldX, worldY |
| onTouchEnd | 触摸结束事件，参数：id, worldX, worldY |
| onTouchMove | 触摸移动事件，参数：id, worldX, worldY |

## 方法
| 方法名 | 作用 |
| ------------- |-------------|
| [isAnyTouch](Touch_isAnyTouch.md) | 当前是否有在触摸 |
| [isAnyTouchStart](Touch_isAnyTouchStart.md) | 当前帧是否有开始触摸 |
| [isTouchStart](Touch_isTouchStart.md) | 某个触摸事件是否开始了 |
| [getTouchById](Touch_getTouchById.md) | 通过ID获取触摸事件 |
| [getTouchByDeviceId](Touch_getTouchByDeviceId.md) | 通过设备ID获取触摸事件 |

## 触摸事件ID
| 定义 | 描述 |
| ------------- |-------------|
| Touch.MAIN | 主触摸事件Id |
