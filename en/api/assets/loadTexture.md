# [qc.Assets](Assets.md)#loadTexture

## Prototype
* void loadTexture(url);
* void loadTexture(url, callback);
* void loadTexture(IMG);
* void loadTexture(IMG, callback);
* void loadTexture(key, url);
* void loadTexture(key, url, callback);
* void loadTexture(key, IMG, callback);

## Parameter
| Parameter | type | Description |
| ------------- | ------------- | -------------|
| key | string | Key of resource|
| url | string | Url of resource. |
| IMG | DOM | The image DOM. |
| callback | function | Callback after resource load successful |


## Description
Asynchronous load a texture from website。

## Example
````javascript
	var url = 'http://www.qcplay.com/Public/Qcplay/images/logo.png';
    self.game.assets.loadTexture(url, function(texture) {
        console.log(texture);
    });
````
