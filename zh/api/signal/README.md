# qc.Signal

## 描述
事件对象。提供事件的派发、广播、监听等功能。如下代码创建了一个事件：
````
	var e = new qc.Signal();
````

## 方法
| 方法名 | 作用 |
| ------------- |-------------|
| [add](add.md) | 添加一个事件监听 |
| [has](has.md) | 是否有某个监听器 |
| [addOnce](addOnce.md) | 添加一个事件监听，触发后自动移除关注 |
| [remove](remove.md) | 移除一个事件监听 |
| [removeAll](removeAll.md) | 移除所有的事件监听 |
| [dispatch](dispatch.md) | 派发事件 |

## 范例
````
	// 创建一个事件监听器
	var e = new qc.Signal();

	// 关注事件
	e.add(function(p1, p2) {
		console.log('1. Receive event:', p1, p2);
	});
	e.addOnce(function(p1, p2) {
		console.log('2. Receive event:', p1, p2);
	});

	// 派发2次事件
	e.dispatch('A', 'B');
	e.dispatch('C', 'D');
````