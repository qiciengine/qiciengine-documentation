# [qc.Dropdown](CDropdown.md)#addOptions

## Prototype
* void addOptions(Array options)

## Paramters
| Paramter | Type | Description |
| --------- | --------- | --------- |
| options | Array |  A list of option to add. |

## Description
Add multiple options to the options of the Dropdown.  

## Example
````
	// The options are 'text'
    dropdown.addOptions(['Option A', 'Option B']);

    // The options are 'texture'
    dropdown.addOptions([game.assets.find('icon')]);
````
