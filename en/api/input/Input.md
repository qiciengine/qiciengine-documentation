# qc.Input

## Description
Input manager is responsible for manage keyboard、mouse、touch event. User can use game.input to refer this module.
Note that this module only manage basic event, such as mouse scroll、mouse click、touch click、keyboard event.
Advanced event is supported by [qc.BaseInputModule](../input/BaseInputModule.md)

## Paramters
| Paramter | Type | Description |
| ------------- |-------------|-------------|
| game | [qc.Game](../game/README.md) | Read only. game instance |
| keyboard | [qc.Keyboard](../input/Keyboard.md) | Keyboard object that monitor keyboard event. |
| mouse | [qc.Mouse](../input/Mouse.md) |  Mouse object that minitor mouse event. |
| touch | [qc.Touch](../input/Touch.md) | Touch object that minitor touch event |
| module | [qc.BaseInputModule](../input/BaseInputModule.md) | Advanced event handler |
| cursorPosition | [qc.Point](../input/Pointer.md) |  Current position of cursor in world coordinate|
| wheelDeltaX | number | Delta distance scrolled in axis x in current frame |
| wheelDeltaY | number | Delta distance scrolled in axis y in current frame |
| keyCount | int | The count of key pressed in current frame |
| keyCodes | array | The codes of key pressed in current frame |
| mouseCount | int |  The count of mouse pressed in current frame |
| mouseIds | array |  The ids of mouse pressed in current frame  |
| touchCount | int |  The count of touch pressed in current frame |
| touchIds | array | The ids of touch pressed in current frame |
| pointerCount | int | The count of pointer in current frame, include mouse and touch |
| pointers | array | The ids of pointer in current frame, include mouse and touch |
| enable | boolean | true by default, no event when is false |
| inputting | boolean | Whether is in editing |

## Event
| Event | Description |
| ------------- |-------------|
| onKeyDown | When key is pressed, the event is trigged. Event parameter is (keyCode，charCode) |
| onKeyUp | When key pop up, the event is trigged. Event parameter is (keyCode，charCode) |
| onKeyRepeat | When key keep pressed, the event is trigged repeatly. Event parameter is (keyCode) |
| onCursorMove | When mouse moved, the event is trigged. Event parameter is (pos_x, pos_y) |
| onWheel | When mouse wheel scroll, the event is trigged. Event parameter is (deltaX, deltaY)|
| onPointerDown | When mouse or touch pressed, the event is trigged. Event parameter is (id，pos_x，pos_y)|
| onPointerUp | When mouse or touch poop up, the event is trigged. Event parameter is (id，pos_x，pos_y)|
| onPointerMove | When mouse or touch moved, the event is trigged. Event parameter is (id，pos_x，pos_y) |

## Method
| Method | Description |
| ------------- |-------------|
| [isKeyDown](../input/Input_isKeyDown.md) | Check whether specified key is pressed |
| [isAnyKeyDown](../input/Input_isAnyKeyDown.md) | Check whether any key is pressed in current frame |
| [isAnyKey](../input/Input_isAnyKey.md) | Check whether any key is pressed |
| [isAltDown](../input/Input_isAltDown.md) |Check whether Alt key is pressed |
| [isControlDown](../input/Input_isControlDown.md) |Check whether Control key is pressed |
| [isShiftDown](../input/Input_isShiftDown.md) |Check whether Shift key is pressed |
| [isMetaDown](../input/Input_isMetaDown.md) |Check whether Meta key is pressed |
| [isMouseDown](../input/Input_isMouseDown.md) | Check whether specified mouse is pressed |
| [isAnyMouseDown](../input/Input_isAnyMouseDown.md) | Check whether any mouse is pressed in current frame |
| [isAnyMouse](../input/Input_isAnyMouse.md) | Check whether any mouse is pressed |
| [isTouchStart](../input/Input_isTouchStart.md) | Check whether specified touch is stated |
| [isAnyTouchStart](../input/Input_isAnyTouchStart.md) | Check whether any touch is stated in current frame |
| [isAnyTouch](../input/Input_isAnyTouch.md) | Check whether any touch is stated |
| [isPointerStart](../input/Input_isPointerStart.md) | Check whether specified pointer is stated |
| [isAnyPointerStart](../input/Input_isAnyPointerStart.md) | Check whether any pointer is stated in current frame |
| [isAnyPointer](../input/Input_isAnyPointer.md) | Check whether any pointer is stated |
| [hasCursor](../input/Input_hasCursor.md) | Check whether cursor is existed |
| [isMouse](../input/Input_isMouse.md) | Check whether specified id is mouse |
| [getPointer](../input/Input_getPointer.md) | Get pointer by id |
  
## Example
````
    // like: game.input.onKeyDown.add(function(keyCode){})
    // But 'addListener' function is recommended, because it will remove event listener automatically. 
    // 'this' is object of qc.Node or qc.Behaviour
    this.addListener(game.input.onKeyDown, function(keyCode) {
    });

    if (game.input.isAnyMouseDown())
    {
        // 。。。。
    }

````

## Manual
[Input and Interaction](http://docs.qiciengine.com/manual/Input/index.html)