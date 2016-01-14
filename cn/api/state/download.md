# [qc.StateManager](README.md).download

## 原型
* void download(state:string, callback:function);

## 参数
| 参数名 | 类型 | 说明 |
| ------------- | ------------- | -------------|
| state | string | 待下载的场景的名称 |
| callback | function、undefined | 下载成功后的回调 |

## 说明
下载场景

## 范例
````
	game.state.download(game.state.entry, function(asset) {
        console.log('Download ok.');
    });
````
