# 本地存储
游戏需要将数据进行保存，如果是单机游戏只能选择保存在本机，网络游戏可以选择保存到服务端。
这里我们提供的是本机的保存接口。  

__注意：__  
* 清除浏览器缓存，本地存储会被清除
* 不同的游戏需要设置不同的game.bundleIdentifier值，否则数据会冲突，参见[工程设置](../Settings/index.html)
* 如果本地缓存容量不足或者手机开启了私密模式，调用相关接口会报异常，开发者有责任处理这种异常情况

## 使用范例
````javascript
	// 设置两条数据
	game.storage.set('name', 'QICI Engine');
	game.storage.set('mixed', {
		year: 2001,
		month: 10
	});

	// 存盘操作
	game.storage.save();

	// 检索字段，返回：'QICI Engine'
	game.storage.get('name');

	// 删除一条记录
	game.storage.del('name');
````

## 模块
[game.storage](http://docs.zuoyouxi.com/api/storage/index.html)
