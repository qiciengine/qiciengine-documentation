# [qc.Animator](Animator.md).play

## 原型  
* void play(int|string|undefined nameOrIndex, [qc.Node](../gameobject/CNode.md) targetObject, boolean fromBegin)

## 参数   
| 参数名         |   类型      |  作用        |
| ------------- | ------------- | -------------|
| nameOrIndex | int or string or undefined | 动作名或动作索引。 |
| targetObject | [qc.Node](../gameobject/CNode.md) | 播放动作的目标对象 |
| fromBegin | boolean | 是否从头播放，默认为 true。 |

## 描述  
播放一个指定的动作。    

## 样例  
````
    // play first action
	this.gameObject.Animator.play();
	
	// play first action
	this.gameObject.Animator.play(0);
	
	// play 'testAction' action
	this.gameObject.Animator.play('testAction')
````
