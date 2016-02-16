# Animator 组件    
如果我们想在某个对象上播放 _动作剪辑_ 或 _动作管理器剪辑_ 文件时，必须为对象挂载一个 Animator 组件。如下图所示：  
![](image/animator.png)  
Animators 可以指定多个 _动作剪辑_ 或 _动作管理器剪辑_ 文件，即一个对象可以播放多个 _动作剪辑_ 或 _动作管理器剪辑_。  
_动作剪辑_ 文件由 [动作编辑器](ActionEditor.md) 生成；_动作管理器剪辑_ 文件由 [动作管理器](ActionManager.md) 生成。

## API  
* 获得指定的 action 对象，可指定动作名或Animators 数组索引，返回 qc.Action 或 qc.ActionManager 对象  
原型：getAction(nameOrIndex)   
nameOrIndex：动作名或 Animators 数组索引  
````javascript
	// get first action
	var action = this.gameObject.Animator.getAction(0);
````  
* 播放指定的动作  
原型：play(nameOrIndex, targetObject, fromBegin)   
nameOrIndex：动作名或 Animators 数组索引，不指定的话默认为 0    
targetObject：动作的目标对象，不指定的话默认为该组件的 gameObject  
fromBegin：是否从头播放，不指定的话默认为 true   
````javascript
	// play first action
	this.gameObject.Animator.play();
````  
* 停止播放指定的动作  
原型：stop(nameOrIndex)   
nameOrIndex：动作名或 Animators 数组索引，不指定的话默认为 0    
````javascript
	// stop first action
	this.gameObject.Animator.stop();
````  

## Demo 
[Action Demo](http://engine.zuoyouxi.com/demo/index.html#anchor_Action)