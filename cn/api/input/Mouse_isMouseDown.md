# [qc.Mouse](Mouse.md).isMouseDown

## 原型
* boolean isMouseDown(id: int);

## 参数
| 参数 | 类型 | 说明 |
| --- | ---- | ---- |
| id | number | 需要检测的鼠标按键，参见：[qc.Mouse](Mouse.md)中定义 |

## 说明
判定当前某个鼠标是否处于按下状态。

## 范例
````
	if (game.input.mouse.isMouseDown(qc.Mouse.BUTTON_LEFT)) {
		console.log('Left mouse button pressed.');
	}
````

