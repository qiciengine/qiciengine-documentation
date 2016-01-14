# [qc.Assets](Assets.md).find

## Prototype
* object find(string key_or_url);

## Parameter
| Parameter | type | Description |
| ------------- | ------------- | -------------|
| key_or_url | string |  Key or Url of resource |

## Description
Find the specified resource. 

## Example
````
	// Use: url
	game.assets.find('Assets/atlas/dota.bin');

	// Use: key
	game.assets.find('dota');
````
