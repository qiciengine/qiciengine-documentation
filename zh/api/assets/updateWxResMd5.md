# [qc.AssetUtil](AssetUtil.md).updateWxResMd5

## 原型
* void updateWxResMd5(game, dislistUrl, assetsMd5Url, callback)

## 参数说明
| 参数名 | 类型 | 说明 |
| ------------- | ------------- | -------------|
| game | qc.Game | 游戏实例 |
| dislistUrl | string | dislist 文件的 url |
| assetsMd5Url | string | assets.md5 文件的 url |
| callback | function | 执行完毕后的回调 |

## 说明
微信小游戏发布后，会自动生成 dislist.dis 和 assets.md5 文件，开发者将这两个文件上传到远程服务器上，此处需要传入这两个文件的 url 地址。 
若函数执行成功，callback 函数会带回 dislist 文件内容。 

