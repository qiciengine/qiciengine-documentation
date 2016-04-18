# [qc.Animator](Animator.md).getAction  

## 原型  
* [qc.Action](../action/Action.md) getAction(int|string nameOrIndex)

## 参数  
| 参数名         |   类型      |  作用        |
| ------------- | ------------- | -------------|
| nameOrIndex | int or string | 动作名或动作索引。 |

## 描述  
根据动作名或动作索引取得动作对象。    

## 样例  
````
    // get first action
	var action = this.gameObject.Animator.getAction(0);
	
	// get action named 'testAction'
	action = this.gameObject.Animator.getAction('testAction');
````
