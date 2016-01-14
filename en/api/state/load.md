# [qc.StateManager](README.md).load

## Prototype
* void load(state:string, clear:boolean, preload:function, create:function);

## Parameters
| Parameter | Type | Description |
| ------------- | ------------- | -------------|
| state | string | The scene to load. |
| clear | boolean | Whether to clear up all cached assets. Default:false. |
| preload | undefined、function | The callback of preload. |
| create | undefined、function | The callback of initialization process. |

## Description
Loads a scene. If the scene has not been downloaded, the function will download first.

## Sample
````
	game.state.load(game.state.entry, true, function() {
        console.log('Start loading assets.');
        game.assets.load('test', 'Assets/atlas/test.bin');
    }, function() {
        console.log('Loaded ok.');
    });
````
