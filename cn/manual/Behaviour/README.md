# 自定义逻辑脚本
引擎提供了接口：qc.defineBehaviour来定义一个界面逻辑脚本。  
__界面逻辑脚本__：用来处理界面相关的组织、显示等逻辑，这脚本需要挂载到相应的Node节点才能起效。通过界面脚本，可以在Inspector面板实时查看和修改数据。  

## 定义和使用逻辑脚本

qc.defineBehaviour接收4个参数：  
1. 脚本的类名
2. 脚本的基类，如果未指定默认为qc.Behaviour（所有界面逻辑脚本都必须以此类作为上层基类）
3. 脚本的构造函数，用来完成一些公共的初始化信息（此函数调度时，脚本尚未被挂载到Node节点，也未完成反序列化）
4. 本脚本需要序列化的属性列表和属性类型  
````javascript
// 定义了一个界面逻辑脚本：qc.demo.OnCollide
// 需要序列化一个属性名为clue，引用了场景中其他Node节点
var OnCollide = qc.defineBehaviour('qc.demo.OnCollide', qc.Behaviour, function() {
    this.clue = null;
}, {
    clue: qc.Serializer.NODE
});
````

添加脚本到节点:  
````javascript
var script = node.addScript('qc.demo.OnCollide');
````

获取脚本对象  
````javascript
var script = getScript('qc.demo.OnCollide');
````

删除节点脚本
````javascript
node.removeScript(script);
````

## 面向组件式编程
区别于传统的面向过程、面向对象编程，behaviour展现了全新的面向组件式编程。通过给对象挂载不同的Behaviour，使其具备不同的表现能力，并且这些功能是可热插拔。  
举个简单的例子，一个空的Image节点只具备显示图片的功能：  
1. 挂载一个behaviour，并实现onClick函数。那么此节点就具备交互功能；
2. 挂载一个动画behaviour，那么此节点就具备动画功能；
3. ...  

更进一步来讲，创建一个自定义组件行为，我们不是通过“继承”的方式进行，而是通过behaviour组合的方式来实现。其强大与灵活之处，请在各例子中仔细体验。

## Behaviour的内置行为
* __帧回调（preUpdate、update、postUpdate）__  
如果实现了这几个函数，系统会自动每帧进行调度（当挂载的Node节点处于可见、并且本脚本的enable=true时）  
* __初始化（awake）__  
如果实现了awake函数，系统会在Node节点构建完毕（反序列化完成后）自动调度  
* __脚本可用/不可用（onEnable、onDisable）__  
当脚本的enable从false->true时，会自动调用onEnable函数；反之调用onDisable函数  
* __交互回调（onClick、onUp、onDown、onDrag、onDragStart、onDragEnd）__  
当挂载的Node具备交互时，一旦捕获相应的输入事件，这些函数会自动被调用  
* __脚本析构（onDestroy）__  
当脚本被移除时，会自动调用onDestroy函数，用户可以定义必要的资源回收代码