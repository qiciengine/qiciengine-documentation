# [qc.Assets](Assets.md).load

## 原型
* void load(url);
* void load(url, callback);
* void load(key, url);
* void load(key, url, callback);

## 参数说明
| 参数名 | 类型 | 说明 |
| ------------- | ------------- | -------------|
| key | string | 资源的关键字，如果不指定则key=url |
| url | string | 待查找资源的url |
| callback | function | 资源加载成功后的回调，参数指明了加载后的资源对象 |

## 说明
异步加载指定资源。

## 范例
````
    // 不关心结果
    game.assets.load('Assets/atlas/dota.bin');

    // 指明key = dota，后续可以通过find('dota')查找到资源对象
    game.assets.load('dota, 'Assets/atlas/dota.bin');

    // 指定加载完成的回调
	game.assets.load('dota', 'Assets/atlas/dota.bin', function(asset) {
		// asset为加载成功后的资源，如果asset=undefined，那么就是加载失败了
		console.log(asset);
		game.log.trace('Load ok.');
	});
````
详细资源加载描述参见[资源加载方式](../../manual/AssetsLoad/index.html)
