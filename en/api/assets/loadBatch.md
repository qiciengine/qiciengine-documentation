# [qc.Assets](Assets.md).loadBatch

## Prototype
* void loadBatch(items, callback)

## Parameter
| Parameter | type | Description |
| ------------- | ------------- | -------------|
| items | array | The array of resource info |
| callback | function 、undefined | Callback after resource load successful |

## Description
Asynchronous load resource in batch.

## Example
````
        var items = [
            {
                key : 'pic',
                url : 'Assets/atlas/pic.bin'
            },
            {   key : 'pic2',
                url : 'Assets/atlas/pic2.bin'
            }
        ];

	game.assets.load(items, function() {
            // save asset array
            var assetArray = [];
            for (var i = 0; i < items.length; i++) {
                assetArray.push(items[i].asset);
            }
	});
````
