# Ellipse

## 描述
描述一个椭圆

## 构造函数
````
	var ellipse = new qc.Ellipse(0, 0, 1, 2);
````

## 变量
| 变量名        |   类型       |  作用           |
| ------------- |-------------|-------------|
| x | number | 圆心X坐标 |
| y | number | 圆心Y坐标 |
| width | number | 长度 |
| height | number | 高度 |

## 方法调用范例
````
	// 检测一个点是否在椭圆内
	ellipse.contains(1, 1);
````