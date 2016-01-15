# [qc.Storage](Storage.md).set

## 原型
* void set(string key, object value)

## 参数说明
| 参数名 | 类型 | 说明 |
| ------------- | ------------- | -------------|
| key | string | 数据的索引 |
| value | object | 数据的值 |

## 说明
保存一条记录

## 范例
````
	// 保存一条记录
	game.storage.set('name', 'weism');

	// 存盘操作
	game.storage.save();
````
