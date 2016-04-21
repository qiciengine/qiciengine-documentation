# [qc.Assets](Assets.md)#loadTexture

## 原型
* void loadTexture(url);
* void loadTexture(url, callback);
* void loadTexture(IMG);
* void loadTexture(IMG, callback);
* void loadTexture(key, url);
* void loadTexture(key, url, callback);
* void loadTexture(key, IMG, callback);

## 参数说明
| 参数名 | 类型 | 说明 |
| ------------- | ------------- | -------------|
| key | string | 资源的关键字，如果不指定则key=url |
| url | string | 待查找资源的url |
| IMG | DOM | IMG的DOM对象 |
| callback | function | 资源加载成功后的回调，参数指明了加载后的资源对象 |

## 说明
异步加载指定原始资源。
__注意：如果资源路径在另外域名下，可能会引发跨域问题（WebGL渲染模式下）__

## 范例
````
    var url = 'http://www.qcplay.com/Public/Qcplay/images/logo.png';
    self.game.assets.loadTexture(url, function(texture) {
        console.log(texture);
    });
````
