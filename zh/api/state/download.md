# [qc.SceneManager](README.md).download

## 原型
* void download(scene:string, callback:function);

## 参数
| 参数名 | 类型 | 说明 |
| ------------- | ------------- | -------------|
| scene | string | 待下载的场景的名称 |
| callback | function、undefined | 下载成功后的回调 |

## 说明
下载场景

## 范例
````
	game.scene.download(game.scene.entry, function(asset) {
        console.log('Download ok.');
    });
````
