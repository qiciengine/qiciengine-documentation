# qc.InputField
inherit [qc.UIImage](CUIImage.md)

## Descrtiption
Turn a simple label into an interactable input field.

## Create a `InputField`
````
    var inputField = new qc.game.add.inputField(parent);
````

## Variables
|  Variable Name |  Type  |  Description   |
| ---------- | --------- | ---------- |
| state | number  | The state for this object: UIState.NORMAL(normal state), UIState.PRESSED(node is pressed), UIState.DISABLED(node is disable) |
| lineType | number | The LineType used by the InputField: InputField.SINGLE_LINE(single line), InputField.MULTI_LINE(multiline) |
| contentType | number | Specifies the type of the input text content.InputField.STANDARD(Allows all input), InputField.INT(Allow whole numbers), InputField.NUMBER(Allows decimal numbers), InputField.TEL(Allows phone), InputField.EMAIL(The input is used for typing in an email address), InputField.PASSWORD(Allows all input and hides the typed characters by showing them as asterisks characters.) |
| text | string | The current value of the input field. |
| placeholderText | string | The placeholder text |
| characterLimit | number | How many characters the input field is limited to. -1 = infinite. |
| overflow | bool | Text flows freely outside the element. Default: true. |
| isFocused | bool | ture:is editing |
| textComponent | qc.Node | The reference of input text node. |
| placeholder | qc.Node | The reference of placeholder text node. |

## Events
|   Event      |     Description       |
| ------------- |-------------|
| onStateChange | When button's state changed, this event is triggered. |
| onNativeClick | Focus on click event by self. |

## Manual
[InputField](http://docs.qiciengine.com/manual/Sample/InputField.html)