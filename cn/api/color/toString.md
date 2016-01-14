# qc.Color#toString

## 原型
* void toString(patten:string);

## 说明
返回颜色的整数描述

## 范例
````
	var c = new qc.Color('#ffffff');

	// 输出为: RGBA(255,255,255,1)
	c.toString('rgba');

	// 输出为：RGB(255,255,255)
	c.toString('rgb');

	// 输出为：#FFFFFF
	c.toString('#rgb');

	// 输出为：#FFFFFFFF
	c.toString('#argb');
````
