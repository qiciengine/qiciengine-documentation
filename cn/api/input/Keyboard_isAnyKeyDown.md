# [qc.Keyboard](Keyboard.md).isAnyKeyDown
## 原型
* boolean isAnyKeyDown(void)

## 说明
当前帧是否有按键按下。注意：只有在当前帧按下才会返回true，到了下一帧即使还处于按下状态，也将返回false。

## 范例
````
	if (game.input.keyboard.isAnyKeyDown()) {
		console.log('Key down.');
	}
````
