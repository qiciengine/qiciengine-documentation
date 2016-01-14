# [qc.Assets](Assets.md).unload

## Prototype
* void unload(string key_or_url)
* void unload(asset)

## Parameter
| Parameter | type | Description |
| ------------- | ------------- | -------------|
| key_or_url | string | Key or Url of resource|
| asset | * | the asset object |

## Description
Release resource from memory. 

## Example
````javascript
	// use url
	game.assets.unload('Assets/atlas/dota.bin');

	// use key
	game.assets.unload('dota');

	// use object
	game.assets.unload(game.assets.find('Assets/atlas/dota.bin'));
````
