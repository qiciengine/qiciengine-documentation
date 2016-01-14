# qc.PluginManager

## 描述
第三方插件管理，可以使用game.plugins访问本模块的实例

## 插件的定义格式
模板定义如下：
````
	PluginTemplet = function(game, parent) {};
	PluginTemplet.prototype = {
	    preUpdate : function() {

	    },

	    update : function() {

	    },

	    postUpdate : function() {

	    },

	    render : function() {

	    },

	    postRender : function() {

	    },

	    destroy : function() {

	    }
	}
	PluginTemplet.prototype.constructor = PluginTemplet;
````
将上面定义的插件通过 [game.plugins.add](add.md) 函数加入 qc.PluginManager，在游戏帧循环时会依次调用上面的
preUpdate、update、postUpdate、render、postRender 函数。

## 变量
| 变量名        | 类型 | 作用           |
| ------------- |-------------|-------------|
| game | [qc.Game](../Game/README.md) | 游戏实例的引用 |
| plugins | object | 只读。所有的插件列表 |

## 方法
| 方法名 | 作用 |
| ------------- |-------------|
| [add](add.md) | 添加一个插件 |
| [remove](remove.md) | 删除一个插件 |
| [removeAll](removeAll.md) | 删除所有插件 |
