# Point

## 描述
描述一个坐标点

## 构造函数
````
	// 指定X、Y坐标构造一个点
	var pt = new qc.Point(2, 3);
````

## 变量
| 变量名        |   类型       |  作用           |
| ------------- |-------------|-------------|
| x | number | x坐标 |
| y | number | y坐标 |

## 方法调用范例
````
	// 计算与另外一个几何体（有x、y属性即可）之间的距离
	var pt = new qc.Point(0, 0);
	pt.distance(new Point(100, 50));
	pt.distance({ x: 5, y: 8 });

	// 是否和另外一个坐标点重合
	if (pt.equals(new qc.Point(1, 1))) {
		console.log('Yes.');
	}

	// 夹角（弧度）
	pt.angle(new qc.Point(1, 1), false);

	// 夹角（角度）
	pt.angle(new qc.Point(1, 1), true);

	// 绕点(1, 2)旋转90度
	pt.rotate(1, 2, Math.PI/2, false);
	pt.rotate(1, 2, 90, true);
````