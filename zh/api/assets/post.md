# [qc.AssetUtil](AssetUtil.md).post

## 原型
* post(string url, string strData, function onload, function onerror)

## 参数说明
| 参数名 | 类型 | 说明 |
| ------------- | ------------- | -------------|
| url | string | 请求地址 |
| strData | string | post 发送的数据 |
| onload | function | 成功请求的回调，原型为：onload(data) |
| onerror | function | 请求失败的回调，原型为：onerror(XMLHTTPREQUEST xhr) |

## 说明
POST 发送数据
