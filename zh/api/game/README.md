# qc.Game

## 描述
这是游戏的心脏，本对象提供了游戏大部分功能的快捷访问通道。游戏的实例生成代码由编辑器自动完成。

## 构造函数
````
    new qc.Game(width, height, parent, state, transparent, editor, debug, physicsConfig);
````
or
````
    new qc.Game(config);
````
该实例不需要手动创建，在发布游戏时，会自动生成 StartGame.html，在 html 中会自动生成相应的代码，以下为 StartGame.html 中的样例代码：
````
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
````
qici.config 变量也在 StartGame.html 中定义，其中 gameInstance 默认为 "game"，用户可在编辑器工程设置中配置游戏实例名，
当使用默认的 "game" 时，可使用全局的 game 变量来引用 qc.Game 这个实例

## 变量
| 变量名 | 作用 |
| ------------- |-------------|
| log: [qc.Log](../log/README.md) | 只读。[日志模块](../log/README.md) |
| debug: [qc.Debug](../debug/README.md) | 只读。[调试模块](../debug/README.md) |
| device: [qc.Device](../device/README.md) | 只读。[设备信息](../device/README.md) |
| add: [qc.GameObjectFactory](../gameobject/GameObjectFactory.md) | 只读。[对象工厂](../gameobject/GameObjectFactory.md) |
| input: [qc.Input](../input/README.md) | 只读。[输入控制模块](../input/README.md) |
| plugins: [qc.PluginManager](../plugin/README.md) | 只读。[插件模块](../plugin/README.md) |
| math: [qc.Math](../math/README.md) | 只读。[数学库](../math/README.md) |
| timer: [qc.Timer](../timer/README.md) | 只读。[定时器模块](../timer/README.md) |
| time: [qc.Time](../time/README.md) | 只读。[时间模块](../time/README.md) |
| sound: [qc.SoundManager](../soundmanager/README.md) | 只读。[声音模块](../soundmanager/README.md) |
| assets: [qc.Assets](../assets/README.md) | 只读。[资源管理](../assets/README.md) |
| stage: [qc.Stage](../stage/README.md) | 只读。[舞台](../stage/README.md) |
| camera: [qc.Camera](../camera/README.md) | 只读。[相机模块](../camera/README.md) |
| world: [qc.World](../world/README.md) | 只读。[游戏世界](../world/README.md) |
| gs: [qc.GS](../gs/README.md) | 只读。[游戏服务器交互模块](../gs/README.md) |
| state: [qc.SceneManager](../state/README.md) | 废弃，请使用scene |
| scene: [qc.SceneManager](../state/README.md) | 只读。[游戏场景管理](../state/README.md) |
| serializer: [qc.Serializer](../serializer/README.md) | 只读。[序列化相关模块](../serializer/README.md) |
| nodePool: [qc.NodePool](../nodepool/README.md) | 只读。[对象池](../nodepool/README.md) |
| storage: [qc.Storage](../storage/README.md) | 只读。[本地存储](../storage/README.md) |
| canvas: Phaser.Canvas | 只读。游戏画布 |
| width: int | 只读。游戏世界的宽度，单位：px |
| height: int | 只读。游戏世界的高度，单位：px |
| resolution: int | 只读。当前游戏的分辨率 |
| transparent: boolean | 游戏的背景是否透明 |
| antialias: boolean | 是否开启抗锯齿 |
| isBooted: boolean | 只读。游戏是否已经启动 |
| isRunning: boolean | 只读。当前游戏是否处于运行状态 |
| paused: boolean | 游戏是否处于暂停状态 |
| parent: string | 只读。游戏的父亲是 DOM 对象，此字段为父亲名字 |
| container: dom | 只读。游戏最外层的dom容器 |
| config: object | 游戏的配置信息 |
| physicsConfig: object | 游戏的物理配置信息 |

## 事件
| 事件名 | 作用 |
| ------------- |-------------|
| onStart | 游戏启动完毕时，触发本事件 |
| onPause | 游戏暂停时，触发本事件 |
| onResume | 游戏暂停结束，触发本事件 |
| onBlur | 游戏窗口失去焦点时，触发本事件 |
| onFocus | 游戏窗口获得焦点时，触发本事件 |


## 方法
| 方法名 | 作用 |
| ------------- |-------------|
| [shutdown](shutdown.md) | 关闭游戏实例 |
