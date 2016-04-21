# qc.Input

## 描述
输入的统一管理类，管理游戏中键盘、鼠标、触摸等操作事件，并将鼠标按下弹起事件和触摸开始结束事件统一为点事件进行处理。
本对象可以通过game.input进行访问。
注意：本类只提供基础事件，例如：鼠标滚动，鼠标、触摸按下，鼠标、触摸弹起等，键盘操作。
高级事件由[qc.BaseInputModule](../input/BaseInputModule.md)提供。

## 变量
| 变量名    | 类型    | 作用           |
| ------------- |-------------|-------------|
| game | [qc.Game](../game/README.md) | 只读。对应的游戏实例 |
| keyboard | [qc.Keyboard](../input/Keyboard.md) | 监控键盘事件的对象 |
| mouse | [qc.Mouse](../input/Mouse.md) | 监控鼠标事件的对象 |
| touch | [qc.Touch](../input/Touch.md) | 监控触摸事件的对象 |
| module | [qc.BaseInputModule](../input/BaseInputModule.md) | 高级事件处理模块 |
| cursorPosition | [qc.Point](../input/Pointer.md) | 当前鼠标光标在世界坐标系中的位置 |
| wheelDeltaX | number | 本帧鼠标在x轴上滚动的距离 |
| wheelDeltaY | number | 本帧鼠标在y轴上滚动的距离 |
| keyCount | int | 本帧按下的键盘按键数量 |
| keyCodes | array | 本帧按下的按键键值 |
| mouseCount | int | 本帧按下的鼠标按键数量 |
| mouseIds | array | 本帧按下的鼠标按键Id |
| touchCount | int | 本帧开始的触摸点数量 |
| touchIds | array | 本帧开始的触摸点Id |
| pointerCount | int | 本帧按下的鼠标和开始的触摸点数量 |
| pointers | array | 本帧按下的鼠标和开始的触摸点Id |
| enable | boolean | 交互开关，默认开启。关闭时，将不产生任何事件 |
| inputting | boolean | 判断当前是否处于编辑状态 |

## 事件
| 事件名 | 作用 |
| ------------- |-------------|
| onKeyDown | 键盘按键按下的事件，派发的参数为按键键值，按键对应的字符（keyCode，charCode） |
| onKeyUp | 键盘按键弹起的事件，派发的参数为按键键值，按键对应的字符（keyCode，charCode） |
| onKeyRepeat | 键盘按键保持按下时触发连击的事件，派发的参数为按键键值，按键对应的字符（keyCode） |
| onCursorMove | 鼠标光标移动的事件，派发的参数为鼠标的x轴位置y轴位置（x，y） |
| onWheel | 鼠标中间滚动的事件，派发的参数为x轴滚动距离，y轴滚动距离（deltaX，deltaY）|
| onPointerDown | 鼠标按下或者触摸开始的事件，派发的参数为鼠标或者光标id，x轴位置，y轴位置（id，x，y）|
| onPointerUp | 鼠标弹起或者触摸结束的事件，派发的参数为鼠标或者光标id，x轴位置，y轴位置（id，x，y）|
| onPointerMove | 鼠标按下移动或者触摸移动的事件，派发的参数为鼠标或者光标id，x轴位置，y轴位置（id，x，y）|

## 方法
| 方法名 | 作用 |
| ------------- |-------------|
| [isKeyDown](../input/Input_isKeyDown.md) | 指定按键是否处于按下状态 |
| [isAnyKeyDown](../input/Input_isAnyKeyDown.md) | 本帧是否有按键按下 |
| [isAnyKey](../input/Input_isAnyKey.md) | 是否有任意按键处于处于按下状态 |
| [isAltDown](../input/Input_isAltDown.md) | Alt是否处于按下状态 |
| [isControlDown](../input/Input_isControlDown.md) | Control是否处于按下状态 |
| [isShiftDown](../input/Input_isShiftDown.md) |  Shift 是否处于按下状态 |
| [isMetaDown](../input/Input_isMetaDown.md) |  Meta是否处于按下状态 |
| [isMouseDown](../input/Input_isMouseDown.md) | 指定鼠标按键是否被按下 |
| [isAnyMouseDown](../input/Input_isAnyMouseDown.md) | 本帧是否有鼠标被按下 |
| [isAnyMouse](../input/Input_isAnyMouse.md) | 是否有任意鼠标处于按下状态 |
| [isTouchStart](../input/Input_isTouchStart.md) | 指定触摸点是否处于开始状态 |
| [isAnyTouchStart](../input/Input_isAnyTouchStart.md) | 本帧是否有触摸点开始 |
| [isAnyTouch](../input/Input_isAnyTouch.md) | 是否有任意触摸点处于开始状态 |
| [isPointerStart](../input/Input_isPointerStart.md) | 是否有指定的鼠标或者触摸点处于开始状态 |
| [isAnyPointerStart](../input/Input_isAnyPointerStart.md) | 本帧是否有鼠标或者触摸点处于开始状态 |
| [isAnyPointer](../input/Input_isAnyPointer.md) | 是否有任何鼠标或者触摸点处于开始状态 |
| [hasCursor](../input/Input_hasCursor.md) | 当前是否有光标的存在，仅当存在鼠标并且鼠标有移动过时为真 |
| [isMouse](../input/Input_isMouse.md) | 指定的事件id是否为鼠标事件 |
| [getPointer](../input/Input_getPointer.md) | 根据事件id获取鼠标或者触摸事件 |
  
## 范例
````
    // 比如: game.input.onKeyDown.add(function(keyCode){})
    // 但是推荐使用 qc.Node 或 qc.Behaviour 中的 'addListener' 方法，因为该方法在对象析构时会自动移除事件关注  
    // this 是 qc.Node 或 qc.Behaviour 对象
    this.addListener(game.input.onKeyDown, function(keyCode) {
        // keyCode 键被按下
    });

    if (game.input.isAnyMouseDown())
    {
        // 。。。。
    }

````

## 参考手册
[输入与交互](http://docs.zuoyouxi.com/manual/Input/index.html)