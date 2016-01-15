# [qc.Assets](Assets.md)#unload

## 原型
* void unload(key_or_url)
* void unload(asset)

## 参数说明
| 参数名 | 类型 | 说明 |
| ------------- | ------------- | -------------|
| key_or_url | string | 待删除资源的key或者url |
| asset | * | 待删除的资源对象 |

## 说明
将资源从内存中释放。

## 范例
````
    // use key
	game.assets.unload('dota');

    // use url
	game.assets.unload('Assets/atlas/dota.bin');

	// use object
	game.assets.unload(game.assets.find('Assets/atlas/dota.bin'));
````
