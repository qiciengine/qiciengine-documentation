# [qc.Assets](Assets.md).find

## 原型
* object find(key_or_url);

## 参数说明
| 参数名 | 类型 | 说明 |
| ------------- | ------------- | -------------|
| key_or_url | string | 待查找资源的key或者url |

## 说明
查找指定资源。

## 范例
````
    // Use: url
	game.assets.find('Assets/atlas/dota.bin');

    // Use: key
    game.assets.find('dota');
````
