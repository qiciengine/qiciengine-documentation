# Line

## 描述
描述一条直线

## 构造函数
````
	var line = new qc.Line(0, 0, 1, 1);
````

## 变量
| 变量名        |   类型       |  作用           |
| ------------- |-------------|-------------|
| start | [qc.Point](Point.md) | 起始点 |
| end | [qc.Point](Point.md) | 结束点 |
| length | number | 只读。长度 |
| angle | number | 只读。弧度 |
| width | number | 只读。水平长度 |
| height | number | 只读。垂直高度 |

## 方法调用范例
````
	var line = new qc.Line(0, 0, 0, 0);

	// 根据起始点、长度、弧度来设置直线
	line.fromAngle(0, 0, Math.PI/2, 100);

	// 相对于另外一条直线的反射直线
	line.reflect(new qc.Line(1, 1, 5, 4));

	// 某个点是否在直线上
	line.pointOnLine(1, 5);
````