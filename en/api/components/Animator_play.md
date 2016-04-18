# [qc.Animator](Animator.md).play

## Prototype
* void play(int|string|undefined nameOrIndex, [qc.Node](../gameobject/CNode.md) targetObject, boolean fromBegin)

## Parameter
| Parameter | type | Description |
| ------------- | ------------- | -------------|
| nameOrIndex | int or string or undefined | The action's Name or the action's index. |
| targetObject | [qc.Node](../gameobject/CNode.md) | The targetObject of action. |
| fromBegin | boolean | Whether to play from begin. It's true by default. |

## Description
Play a specified action.  

## Example
````
    // play first action
	this.gameObject.Animator.play();
	
	// play first action
	this.gameObject.Animator.play(0);
	
	// play 'testAction' action
	this.gameObject.Animator.play('testAction')
````
