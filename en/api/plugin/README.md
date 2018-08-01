# qc.PluginManager

## Description
The Plugin Manager is responsible for the loading, running and unloading of Plugins.

## Define a plugin
The templete:
````
	PluginTemplete = function(game, parent) {};

	PluginTemplete.prototype.init = function() {

	};

	PluginTemplete.prototype.preUpdate = function() {

	};

	PluginTemplete.prototype.update = function() {
			console.log('update');
	};

	PluginTemplete.prototype.postUpdate = function() {

	};

	PluginTemplete.prototype.render = function() {

	};

	PluginTemplete.prototype.postRender = function() {

	};

	PluginTemplete.prototype.destroy = function() {

	};

	PluginTemplete.prototype.constructor = qc.NodeScheduler;
````

## Variables
| Variable Name  | Type | Description  |
| ------------- |-------------|-------------|
| game | [qc.Game](../game/README.md) | The local game reference. |
| plugins | object | Read only. The list of all plugins. |

## Methods
| Method | Description |
| ------------- |-------------|
| [add](add.md) | Add a new Plugin into the PluginManager. |
| [remove](remove.md) | Remove a Plugin from the PluginManager. |
| [removeAll](removeAll.md) | Remove all Plugins from the PluginManager. |
