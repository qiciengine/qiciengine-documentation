# [qc.ScrollView](CScrollView.md).setNormalizedPosition

## 原型
* void setNormalizedPosition(number value, int axis)

## 参数
| 参数名 | 类型 | 说明  |
| --------- | --------- | --------- |
| value | number | 设置的值 |
| axis |  int | 坐标轴， 0:x轴，1:y轴 |

## 描述
设置指定方向上的滚动值。

## 范例
````
	// 在X方向滚动到50%位置
	node.setNormalizedPosition(0.5, 0);

	// 在Y方向滚动到60%位置
	node.setNormalizedPosition(0.6, 1);
````
