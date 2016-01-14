# [qc.PluginManager](README.md).add

## Prototype
* void add(object plugin, params...)

## Parameters
| Parameter | Type | Description |
| --- | ---- | ---- |
| plugin | object | The Plugin to add into the PluginManager.  |
| params... | any| Additional parameters that will be passed to the Plugin.init method. |

## Description
Add a new Plugin into the PluginManager.  
The Plugin must have 2 properties: game and parent. Plugin.game is set to the game reference the PluginManager uses, and parent is set to the PluginManager.