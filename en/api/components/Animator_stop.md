# [qc.Animator](Animator.md).stop

## Prototype
* void stop(int|string|undefined nameOrIndex)

## Parameter
| Parameter | type | Description |
| ------------- | ------------- | -------------|
| nameOrIndex | int or string or undefined | The action's Name or the action's index. |

## Description
Stop a specified action.  

## Example
````
    // stop first action
	this.gameObject.Animator.stop();
	
	// stop action named 'testAction'
	this.gameObject.Animator.stop('testAction');
````
