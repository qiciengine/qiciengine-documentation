# qc.PluginManager

## Description
The Plugin Manager is responsible for the loading, running and unloading of Plugins.

## Define a pulgin
The templete:
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
	PluginTemplet.prototype.constructor = qc.NodeScheduler;
````

## Variables
| Variable Name  | Type | Description  |
| ------------- |-------------|-------------|
| game | [qc.Game](../Game/README.md) | The local game reference. |
| plugins | object | Read only. The list of all plugins. |

## Methods
| Method | Description |
| ------------- |-------------|
| [add](add.md) | Add a new Plugin into the PluginManager. |
| [remove](remove.md) | Remove a Plugin from the PluginManager. |
| [removeAll](removeAll.md) | Remove all Plugins from the PluginManager. |
