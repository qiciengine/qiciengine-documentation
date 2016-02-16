# 输入控制

## 描述
游戏中的交互管理组件，提供键盘、鼠标、触摸等操作的控制。  
[qc.Input](../input/Input.md)已经将常用的操作进行封装，一般使用此模块就足够。

## 类
| 类名     | 作用           |
| ------------- | -------------|
| [qc.Input](../input/Input.md) | 基础事件管理类，提供键盘、鼠标、触摸等基础事件 |
| [qc.BaseInputModule](../input/BaseInputModule.md) | 高级事件管理类，提供拖拽、点击等事件 |
| [qc.Keyboard](../input/Keyboard.md) | 键盘 事件监听及管理 |
| [qc.Mouse](../input/Mouse.md) | 鼠标事件监听及管理 |
| [qc.Touch](../input/Touch.md) | 触摸事件监听及管理 |
| qc.Key | 按键事件对象 |
| [qc.Pointer](../input/Pointer.md) | 鼠标和触摸事件对象 |
| [qc.BaseInputEvent](../input/BaseInputEvent.md) | 交互事件的基础类 |
| [qc.WheelEvent](../input/WheelEvent.md) | 鼠标滚轮事件 |
| [qc.CursorMoveEvent](../input/CursorMoveEvent.md) | 光标移动事件 |
| [qc.PointerEvent](../input/PointerEvent.md) | 鼠标或者触摸事件 |
| [qc.DragStartEvent](../input/DragStartEvent.md) | 拖拽开始事件 |
| [qc.DragEndEvent](../input/DragEndEvent.md) | 拖拽结束事件 |
| [qc.DragEvent](../input/DragEvent.md) | 拖拽移动事件 |
| [qc.DropEvent](../input/DropEvent.md) | 拖拽放下事件 |

## 相关范例
[Demo](http://engine.zuoyouxi.com/demo/index.html#Input)

