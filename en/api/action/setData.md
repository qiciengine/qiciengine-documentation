# [qc.Action](Action.md).setData

## Prototype
* void setData(path, propertyId, attrib, data)

## Parameter
| Parameter | type | Description |
| ------------- | ------------- | -------------|
| path | string | The path of hierarchy. The targetObject's path is '/'. If targetObject has a child named 'childSprite', then childSprite's path is '/childSprite' |
| propertyId | int | Constant define of action property. See [Action Properties](actionDef.md) |
| attrib | string | The detail attrib of propertyId. See [Action Properties](actionDef.md)|
| data | mapping | The data for Action's property |

## Description
Set specific data for specific property of action. The method generally is used to set from and to value of property whose curveType is TweenAbsolute or TweenRelative. See: [Instruction for Curve Type](http://docs.qiciengine.com/manual/Action/ActionEditor.html#instruction-for-curve-type).


## Example
````javascript
	// get test action
	var action = this.gameObject.Animator.getAction('test');
	
	// If curveType of x attrib is TweenAbsolute in the action clip, we can set from、to parameters for the action 
	action.setData('/', qc.PROP_POSITON, 'x', { from : 0, to : 100 });
	
	// If curveType of x attrib is TweenRelative in the action clip, we can set to parameters for the action 
	action.setData('/', qc.PROP_POSITON, 'x', { to : 100 });
	
	// play test action
	this.gameObject.Animator.play('test');
````  