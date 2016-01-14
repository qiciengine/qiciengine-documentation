# [qc.AssetUtil](AssetUtil.md).post

## Prototype
* post(string url, string strData, function onload, function onerror)

## Parameter
| Parameter | Type | Description |
| ------------- | ------------- | -------------|
| url | string | The address of request |
| strData | string | The data need to post |
| onload | function | The callback of succeed. Prototype is : onload(data) |
| onerror | function | The callback of fail. Prototype is : onerror(XMLHTTPREQUEST xhr) |

## Description
Send POST request.
