# [qc.Mouse](Mouse.md).isAnyMouseDown

## 原型
* boolean isAnyMouseDown(void);

## 说明
判定当前帧是否有鼠标处于按下状态。需要注意的是，第一次按下时本帧判定会返回true，到了下一帧就是false了。

## 范例
````
	if (game.input.mouse.isAnyMouseDown()) {
		console.log('Mouse pressed.');
	}
````
