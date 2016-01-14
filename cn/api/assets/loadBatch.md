# [qc.Assets](Assets.md).loadBatch

## 原型
* void loadBatch(items)
* void loadBatch(items, callback)

## 参数说明
| 参数名 | 类型 | 说明 |
| ------------- | ------------- | -------------|
| items | array |资源信息数组 |
| callback | function | 资源加载成功后的回调 |

## 说明
批量加载资源。

## 范例
````
    var items = [
        {
            key : 'pic',
            url : 'Assets/atlas/pic.bin'
        },
        {
            url : 'Assets/atlas/pic2.bin'
        }
    ];

	game.assets.load(items, function() {
        // 保存图集数组
        var assetArray = [];
        for (var i = 0; i < items.length; i++) {
            assetArray.push(items[i].asset);
        }
	});
````
