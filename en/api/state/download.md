# [qc.StateManager](README.md).download

## Prototype
* void download(scene:string, callback:function);

## Parameters
| Parameter | Type | Description |
| ------------- | ------------- | -------------|
| scene | string | The scene to download. |
| callback | function、undefined | The callback of download successful. |

## Sample
Downloads a scene asset.

## Sample
````
	game.scene.download(game.scene.entry, function(asset) {
        console.log('Download ok.');
    });
````
