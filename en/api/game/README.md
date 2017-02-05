# qc.Game

## Description

This is the heart of the game, which provides a large part of fast functional access channel.
The instance of `qc.Game` is automatically constructed by editor.

## Prototype

* `qc.Game(width, height, parent, state, transparent, editor, debug, physicsConfig);`
* `qc.Game(config);`

The game instance does not need to be created manually. It will be automatically created in StartGame.html which is created when a game get [published](http://docs.qiciengine.com/manual/Publish/index.html).

The following sample code for StartGame.html

````javascript
        qici.loadGame = function() {
        var game = window[qici.config.gameInstance] = new qc.Game({
            width: '100%',
            height: '100%',
            parent: 'gameDiv',
            state: qici.splashState,
            editor: qici.config.editor === true,
            backgroundColor: new qc.Color(qici.config.backgroundColor),
            runInBackground: qici.config.runInBackground,
            antialias: qici.config.antialias,
            resolution : qici.config.resolution,
            transparent: qici.config.transparent,
            debug: qici.config.developerMode === true,
            renderer: (function() {
                if (qici.config.renderer === 'WebGL') {
                    return Phaser.WEBGL;
                }
                if (qici.config.renderer === 'Canvas'){
                    return Phaser.CANVAS;
                }
                return Phaser.AUTO;
            })()
        });

        game.loadingProcessCallback = qici.loadAssetsNotify;
        game.bundleIdentifier = qici.config.bundleIdentifier;
        game.log.important('**** [QICI Engine]Starting game: {0}', qici.config.gameName);
    };
```

`qici.config` variable is also defined in StartGame.html. gameInstance variable is 'game' by default. User can configure the game instance name in the editor project settings.
When using the default 'game' name, you can use the global game variable to refer to the instance of `qc.Game`.

## Variables
| Variable name | Description |
| ------------- |-------------|
| log: [qc.Log](../log/README.md) | Read only. [Log Management](../log/README.md) |
| debug: [qc.Debug](../debug/README.md) | Read only. [Debug Management](../debug/README.md) |
| device: [qc.Device](../device/README.md) | Read only. [Device Information](../device/README.md) |
| add: [qc.GameObjectFactory](../gameobject/GameObjectFactory.md) | Read only. [Objects Factory](../gameobject/GameObjectFactory.md) |
| input: [qc.Input](../input/README.md) | Read only. [Input Management](../input/README.md) |
| plugins: [qc.PluginManager](../plugin/README.md) | Read only. [Plugins Management](../plugin/README.md) |
| math: [qc.Math2](../math/README.md) | Read only. [Math Library](../math/README.md) |
| timer: [qc.Timer](../timer/README.md) | Read only.[Timer](../timer/README.md) |
| time: [qc.Time](../time/README.md) | Read only.[Time](../time/README.md) |
| sound: [qc.SoundManager](../soundmanager/README.md) | Read only.[Sound Manager](../soundmanager/README.md) |
| assets: [qc.Assets](../assets/README.md) | Read only. [Assets Management](../assets/README.md) |
| stage: qc.Stage |  Read only. Stage |
| world: [qc.World](../world/README.md) | Read only. [Game World](../world/README.md) |
| gs: qc.GS | Read only. The connector of game server|
| state: [qc.StateManager](../state/README.md) | Obsolete. |
| scene: [qc.SceneManager](../state/README.md) | Read only. [Scenes Management](../state/README.md) |
| serializer: [qc.Serializer](../serializer/README.md) | Read only. [Serializer](../serializer/README.md) |
| nodePool: qc.NodePool| Read only. NodePool |
| storage: [qc.Storage](../storage/README.md) | Read only. [Local Storage Management](../storage/README.md) |
| canvas: Phaser.Canvas |  Read only.  |
| width: int | The width of game world. Unit:px |
| height: int | The height of game world. Unit:px |
| transparent: boolean | true: the game background is transparent. |
| antialias: boolean | Draw all image textures anti-aliased or not. |
| isBooted: boolean | Read only. true: the game is booted|
| isRunning: boolean | Read only. true: the game is running.  |
| paused: boolean | true: the game is paused. |
| config: object | Configuration information of the game. |
| physicsConfig: object | Physics config information of the game. |

## Events
| Event name | Description |
| ------------- |-------------|
| onStart | When the game is started, this event is triggered. |
| onPause | When the game is paused, this event is triggered. |
| onResume | When resuming the game, this event is triggered. |
| onBlur | When the game loses the focus, this event is triggered. |
| onFocus | When the game receives the focus, this event is triggered. |

## Mehtods
| Method | Description |
| ------------- |-------------|
| [shutdown](shutdown.md) | Shut down the game. |
