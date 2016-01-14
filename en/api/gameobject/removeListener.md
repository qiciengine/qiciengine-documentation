# qc.Node#removeListener

## Prototype
* void removeListener([int]id);

## Paramters
| Paramter | Type | Description |
| ------------- | ------------- | -------------|
| id | int | Listener ID |

## Description
Remove listener manually.

## Example
````
    var id = this.addListener(this.game.input.onKeyDown, function(keycode){
            console.log('key down');
    });
	
	this.removeListener(id);
````
