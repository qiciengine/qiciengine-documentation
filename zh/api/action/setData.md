# [qc.Action](Action.md).setData

## 原型
* void setData(path, propertyId, attrib, data)

## 参数说明
| 参数名 | 类型 | 说明 |
| ------------- | ------------- | -------------|
| path | string | 节点层级路径。动作剪辑的 targetObject 的 path 为 '/'，若 targetObject 有一个子节点 childSprite，则 childSprite 的 path 为 '/childSprite' |
| propertyId | int | 动作属性的宏定义，见[动作属性定义](actionDef.md) |
| attrib | string | propertyId 动作属性下的具体属性，见[动作属性定义](actionDef.md) |
| data | mapping | 设置的数据，数据的内容取决于不同的动作属性所需的参数 |

## 说明
给 action 对象的指定属性设置数据。主要用于设置 CurveType 为 TweenAbsolute 和 TweenRelative 类型的属性的 from 和 to 值，参考：[数值曲线类型介绍](http://docs.zuoyouxi.com/manual/Action/ActionEditor.html#数值曲线类型介绍)

## 范例
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