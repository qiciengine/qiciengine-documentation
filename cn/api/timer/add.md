# [qc.Timer](README.md).add

## 原型
* qc.TimerEvent add(number delay=, function cb, object context, ...*)

## 参数说明
| 参数名 | 类型 | 说明 |
| ------------- | ------------- | -------------|
| delay | number | 延迟多少毫秒定时器到时 |
| cb | function | 执行的回调函数 |
| context | undefined、object | 回调函数的上下文实例 |
| ...* | 不定参数 | 原样带回给回调函数 |

## 说明
添加一个定时器

## 范例
````
	// 添加一个定时器，1秒后打印一条信息
	var t = game.timer.add(1000, function() {
		console.log('Timer trigger.');
	})
````
