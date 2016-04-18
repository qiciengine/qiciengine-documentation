# [qc.Animator](Animator.md).stop

## 原型  
* void stop(int|string|undefined nameOrIndex)

## 参数     
| 参数名         |   类型      |  作用        |
| ------------- | ------------- | -------------|
| nameOrIndex | int or string or undefined | 动作名或动作索引。 |

## 描述  
停止指定的动作。   

## Example
````
    // stop first action
	this.gameObject.Animator.stop();
	
	// stop action named 'testAction'
	this.gameObject.Animator.stop('testAction');
````
