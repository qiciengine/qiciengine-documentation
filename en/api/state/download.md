# [qc.StateManager](README.md).download

## Prototype
* void download(state:string, callback:function);

## Parameters
| Parameter | Type | Description |
| ------------- | ------------- | -------------|
| state | string | The scene to download. |
| callback | function、undefined | The callback of download successful. |

## Sample
Downloads a scene.

## Sample
````
	game.state.download(game.state.entry, function(asset) {
        console.log('Download ok.');
    });
````
