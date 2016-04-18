# [qc.Animator](Animator.md).getAction

## Prototype
* [qc.Action](../action/Action.md) getAction(int|string nameOrIndex)

## Parameter
| Parameter | type | Description |
| ------------- | ------------- | -------------|
| nameOrIndex | int or string | The action's Name or the action's index. |

## Description
Get a action by action's name or action's index.  

## Example
````
    // get first action
	var action = this.gameObject.Animator.getAction(0);
	
	// get action named 'testAction'
	action = this.gameObject.Animator.getAction('testAction');
````
