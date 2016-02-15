# qc.Dropdown
inherit [qc.UIImage](CUIImage.md)

## Description
A standard dropdown that presents a list of options when clicked, of which one can be chosen.  
When a dropdown event occurs a callback is sent to any registered listeners of onValueChanged.  

## Varialbes
| Variable Name        |   Type       |  Description           |
| ------------- |-------------|-------------|
| state | int  |  The state of dropdown: UIState.NORMAL(normal state), UIState.PRESSED(button pressed), UIState.DISABLED(button is disable) |
| captionImage | qc.UIImage | The Image component to hold the image of the currently selected option. |
| captionText | qc.UIText | The Text component to hold the text of the currently selected option. |
| item | qc.Node | The component to hold the text or the image of the item. |
| options | Array | The list of possible options. A text string and an image can be specified for each option. |
| template | qc.Node | The Transform of the template for the dropdown list. |
| value | int | The index of the currently selected option. 0 is the first option, 1 is the second, and so on. |

## Events
|   Event      |     Description       |
| ------------- |-------------|
| onStateChange | When dropdown's state changed, this event is triggered. |
| onValueChange | When a user has clicked one of the options in the dropdown list, this event is triggered. |

## Methods
| Method | Description |
| ------------- |-------------|
| [addOptions](dropdown_addOptions.md) | Add multiple options to the options of the Dropdown. |
| [clearOptions](dropdown_clearOptions.md) | Clear the list of options in the Dropdown. |
| [show](dropdown_show.md) | Show the dropdown list. |
| [hide](dropdown_hide.md) |Hide the dropdown list. |

## Manual
[Dropdown](http://docs.qiciengine.com/manual/Sample/Dropdown.html)