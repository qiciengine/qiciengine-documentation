# Matrix

## 描述
矩阵描述：
````
	| a | b | tx|
	| c | d | ty|
	| 0 | 0 | 1 |
````
构造函数：
````
	var m = new qc.Matrix();
````

## 变量
| 变量名        |   类型       |  作用           |
| ------------- |-------------|-------------|
| a | number | a，默认1 |
| b | number | b，默认0 |
| c | number | c，默认0 |
| d | number | d，默认1 |
| tx | number | tx，默认0 |
| ty | number | ty，默认0 |


## 方法调用范例
````
	// 数组依次指明了a, b, tx, c, d, ty
	m.fromArray([0, 0, 1, 0, 0, 1]);

	// 乘
	m.apply(new qc.Point(5, 4));

	// 逆
	m.applyInverse(new qc.Point(5, 4));

	// 平移
	m.translate(1, 2);

	// 缩放
	m.scale(1, 1);

	// 旋转
	m.rotate(Math.PI / 2);
````
