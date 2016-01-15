# qc.Mouse

## 描述
鼠标的输入控制。可以通过game.input.mouse访问本实例，常用接口已经在[qc.Input](Input.md)中进行的封装，请优先使用。

| 变量名    | 类型    | 作用           |
| ------------- |-------------|-------------|
| enable | boolean | 鼠标交互开关，默认为true |
| mouseWheel | object |鼠标两帧之间滚动的距离，{deltaX: number, deltaY: number} |
| mouseCount | int | 当前按下的鼠标数量 |
| mouseIds | array | 当前所有按下的鼠标id |

## 事件
| 事件名 | 作用 |
| ------------- |-------------|
| onMouseDown | 鼠标被按下事件，参数：button, worldX, worldY |
| onMouseUp | 鼠标松开事件，参数：button, worldX, worldY |
| onMouseMove | 鼠标移动事件，参数：button, worldX, worldY |
| onMousePressMove | 鼠标按下并移动事件，参数：button, worldX, worldY |
| onMouseWheel | 鼠标滚轮事件，参数：wheelDelta, wheelDeltaX, wheelDeltaY |

## 方法
| 方法名 | 作用 |
| ------------- |-------------|
| [isAnyMouse](Mouse_isAnyMouse.md) | 当前是否有鼠标处于按下状态 |
| [isAnyMouseDown](Mouse_isAnyMouseDown.md) | 当前帧是否有鼠标按下了 |
| [isMouseDown](Mouse_isMouseDown.md) | 某个鼠标是否处于按下状态 |
| [getMouseById](Mouse_getMouseById.md) | 通过ID获取鼠标 |

## 鼠标的ID列表
| 定义 | 描述 |
| ------------- |-------------|
| Mouse.NONE | 没有按下鼠标 |
| Mouse.BUTTON_LEFT | 左键 |
| Mouse.BUTTON_MIDDLE | 中键 |
| Mouse.BUTTON_RIGHT | 右键 |
| Mouse.BUTTON_BACK | 后退键 |
| Mouse.BUTTON_FORWORD | 前进键 |
