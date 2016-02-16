# [qc.Touch](Touch.md).isTouchStart

## 原型
* boolean isTouchStart(id:int)

## 参数
| 参数 | 类型 | 说明 |
| --- | ---- | ---- |
| id | number | 需要检测的触摸事件，参见：[qc.Touch](Touch.md)中定义 |

## 说明
当前指定的触摸事件是否开始了

## 范例
````
	if (game.input.touch.isTouchStart(qc.Touch.MAIN)) {
		console.log('Main Touch.');
	}
````
