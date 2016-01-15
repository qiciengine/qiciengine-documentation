# [qc.StateManager](README.md).load

## 原型
* void load(state:string, clear:boolean, preload:function, create:function);

| 参数名 | 类型 | 说明 |
| ------------- | ------------- | -------------|
| state | string | 目标场景的名称 |
| clear | boolean | 是否将所有缓存的资源清理掉，默认为false |
| preload | undefined、function | 场景预加载的回调，可以在这里指明加载资源等 |
| create | undefined、function | 场景创建时的回调处理 |

## 说明
切换场景，切换时首先下载场景，场景下载完毕后再进行切换操作。

## 范例
````
	game.state.load(game.state.entry, true, function() {
        console.log('Start loading assets.');
        game.assets.load('test', 'Assets/atlas/test.bin');
    }, function() {
        console.log('Loaded ok.');
    });
````
