# Dom节点
qc.Dom节点本质上就是一个div元素，拥有所有HTML元素的特性，由于不需要像普通游戏对象那样每帧都渲染，因此较为高效。  
对于静态的元素，首选使用DOM来实现。	

## 层次
Dom的div元素可置于game.canvas之上或之下，位于game.canvas之上的挂载在game.world.frontDomRoot元素上，位于game.canvas之下的挂载在game.world.backDomRoot元素上。只有当game.cavnas设置为透明的情况下，位于canvas之后的Dom元素才可见，参见[工程设置](../Settings/index.html)
````
	|
	|--- game.world.frontDomRoot (div)
	|
	|--- game.canvas (canvas)
	|
	|--- game.world.backDomRoot (div)
	|
game.container (div normally)
````

## 资源
默认编辑器会自动对游戏资源打包成bin后缀的zip格式，[发布工程](../Publish/index.html)时只会发布zip格式文件，原始资源文件不会被拷贝，但Dom的div元素往往需要访问图片等原始资源，因此Assets/raw作为特殊目录，专门用于存放无需打包的资源内容。

## CSS
Assets/css目录的style.css文件可用于配置所有Dom元素css效果，游戏运行的html页面会自动链接引入该css文件。例如可在Dom的div元素上设置className，然后在style.css上对className进行定义。

## 代码创建Dom对象
````javascript
// 创建一个Dom对象
var dom = game.add.dom();

// 设置Dom对象div元素的innerHTMl内容
dom.div.innerHTML = '<img src='test.png' />';

// 设置Dom对象div元素的风格
dom.div.style.color = 'red';
dom.div.style.padding = '10px';

// 创建Dom对象div元素的子元素
var subDiv = document.createElement('div');
dom.div.appendChild(subDiv);
````

## 编辑器创建Dom对象
![Dom](images/dom.png)

### Hit Area
交互属性，如果在Dom对象中要使用链接，并希望用户点击链接后能跳转，就需要设置Hir Area，打开交互。
*__注意:__* 当打开交互后，该节点上不能再使用onClick等事件，游戏事件会与页面处理冲突，而导致无法达到想要的效果。

### Pos
位置属性，决定Dom位于game.canvas之上或之下：
* qc.Dom.POS_FRONT: 位于game.canvas之上
* qc.Dom.POS_BACK: 位于game.canvas之上

````javascript
node.pos = qc.Dom.POS_FRONT
````

### InnerHTML
用于设置div元素的innerHTML属性，其中的Serializable属性决定是否进行保存，如果Dom的具体内容由其脚本动态生成，Inspector上只需要查看的情况下，可关闭Serializable属性。
````javascript
node.innerHTML = 'QICI Engine';
node.serializable = true;
````

### Overflow
对应div.style.overflow属性，可取值：visible、scroll、hidden或auto
````javascript
node.overflow = 'hidden';
````

### ZIndex
对应div.style.zIndex属性，位于canvas之上时zIndex值需大于0，位于canvas之下时zIndex需小于0。
````javascript
node.zIndex = 1;
````

### ClassName
对应div.className属性
````javascript
node.className = 'qici-logo';
````

## Video
<video controls="controls" src="../video/oper_dom.mp4"></video>  

## API
[Dom API](http://docs.zuoyouxi.com/api/gameobject/CDom.html)

## Demo
[DOM Demo](http://engine.zuoyouxi.com/demo/index.html#anchor_Dom)
