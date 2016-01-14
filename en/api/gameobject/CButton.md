# qc.Button
inherit [qc.UIImage](CUIImage.md)

## Description
A standard button that can be clicked in order to trigger an event.

## Varialbes
| Variable Name        |   Type       |  Description           |
| ------------- |-------------|-------------|
| state | int  |  The state of button: UIState.NORMAL(normal state), UIState.PRESSED(button pressed), UIState.DISABLED(button is disable) |
| text | [qc.UIText](CUIText.md) | The reference text node. |
| supportNativeEvent | bool | Is the button support native event of browser. |

## Events
|   Event      |     Description       |
| ------------- |-------------|
| onStateChange | When button's state changed, this event is triggered. |
| onValueChange | When value changed, this event is triggered. |

## Manual
[Button](http://docs.qiciengine.com/manual/Sample/Button.html)