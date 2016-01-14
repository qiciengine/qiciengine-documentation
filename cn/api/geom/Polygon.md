# Polygon

## 描述
描述一个多边形

## 构造函数
````
	// 指明了多边形的各个顶点
	var polygon = new qc.Polygon(new qc.Point(0, 0), new qc.Point(1, 1), new qc.Point(1, 4));
````

## 变量
| 变量名        |   类型       |  作用           |
| ------------- |-------------|-------------|
| area | number | 面积 |
| closed | boolean | 多边形是否封闭？ |
| points | array | 顶点列表 |

## 方法调用范例
````
	// 点是否在多边形内
	polygon.contains(1, 1);
````