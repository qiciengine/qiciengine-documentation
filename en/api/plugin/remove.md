# [qc.PluginManager](README.md).remove

## Prototype
* void remove(object plugin)

## Parameters
| Parameter | Type | Description |
| --- | ---- | ---- |
| plugin | object | The plugin to be removed. |

## Description
Remove a Plugin from the PluginManager. It calls Plugin.destroy on the plugin before removing it from the manager.