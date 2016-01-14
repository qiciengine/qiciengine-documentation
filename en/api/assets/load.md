# [qc.Assets](Assets.md).load

## Prototype
* void load(string url)
* void load(string url, function callback)
* void load(string key, string url)
* void load(string key, string url, function callback)

## Parameter
| Parameter | type | Description |
| ------------- | ------------- | -------------|
| key | string | Key of resource|
| url | string | Url of resource. |
| callback | function | Callback after resource load successful |
| override | boolean | false by default. Whether to ignore the cached data and force a reload|

## Description
Asynchronous load resource。

## Example
````javascript
	game.assets.load('Assets/atlas/dota.bin');

	// key = dota. 
	game.assets.load('dota, 'Assets/atlas/dota.bin');

	game.assets.load('dota', 'Assets/atlas/dota.bin', function(asset) {
        console.log(asset);
        game.log.trace('Load ok.');
    });
````
Detailed resource loading description see also
[Assets Load](http://docs.qiciengine.com/manual/AssetsLoad/index.html)
