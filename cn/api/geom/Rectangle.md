# Rectangle

## 描述
描述一个矩形

## 构造函数
````
	var rect = new qc.Rectangle(0, 0, 1, 2);
````

## 变量
| 变量名        |   类型       |  作用           |
| ------------- |-------------|-------------|
| x | number | 左上角X坐标 |
| y | number | 左上角Y坐标 |
| width | number | 长度 |
| height | number | 高度 |
| centerX | number | 中心点X坐标 |
| centerY | number | 中心点Y坐标 |

## 方法调用范例
````
	// 移动矩形，让矩形的中心与指定点重合
	rect.centerOn(1，1);

	// 检测一个点是否在矩形内
	rect.contains(1, 1);
````
