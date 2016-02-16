# qc.Assets

## Description
This module handles loading all external content such as Images, Sounds, Texture Atlases and data files.This class represents a singleton object that can be accessed directly as `game.assets`.
The types of assets are as following:
* [Atlas: atlas and animation](Atlas.md)
* [ExcelAsset: Excel](ExcelAsset.md)
* [Prefab](Prefab.md)
* [SoundAsset: audio](SoundAsset.md)
* [TextAsset: text](TextAsset.md)
* [Font](Font.md)

## Variables
| Variable Name       | Type   |    Description        |
| ------------- |-------------|-------------|
| game | [qc.Game](../game/README.md) | Local reference to game. |
| isLoading | boolean | Read only. True if the Loader is in the process of loading the queue. |
| hasLoaded | boolean | Read only. True if all assets in the queue have finished loading. |
| baseURL | string | If you want to append a URL before the path of any asset you can set this here. |
| parsing | boolean | Read only. True if the Loader is in the process of unpacking the queue. |
| loaded | int | Read only. The number of assets that have finished loading. |
| total | int | Read only. The number of all assets in the queue. |
| maxRetryTimes | int | Default 1. |

## Methods
| Method | Description |
| ------------- |-------------|
| [load](load.md) | Asynchronous load resource(ie:image,prefab etc). |
| [loadBatch](loadBatch.md) | batch load resource |
| [find](find.md) | Find asset. |
| [unload](unload.md) | Unload asset. |
| [clear](clear.md) | Clear all assets. |
| [loadTexture](loadTexture.md) | Load a texture from website. |

## Manual
[Asset Management](http://docs.qiciengine.com/manual/AssetsLoad/index.html)