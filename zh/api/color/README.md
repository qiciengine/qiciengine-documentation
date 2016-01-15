# qc.Color

## 描述
颜色的描述类

## 构造函数
````
	// 十六进制字符串描述，大小写都可以
	// 支持: RRGGBB\AARRGGBB
	var c = new qc.Color('#ffffff');
	var c = new qc.Color('#FFFFFF');
	var c = new qc.Color('#CCFFFFFF');

	// 字符串描述RGB
	var c = new qc.Color('rgb(100, 125, 255)');
	var c = new qc.Color('RGB(100, 125, 255)');
	var c = new qc.Color('RGBA(100, 125, 255, 0.5)');
	var c = new qc.Color('rgba(100, 125, 255, 0.5)');

	// 整数描述
	var c = new qc.Color(0xffffff);

	// 数组描述
	// 数组为：[r, g, b, a]
	var c = new qc.Color([125, 100, 255]);
	var c = new qc.Color([125, 100, 255, 0.5]);
````

## 变量
| 变量名         |   类型      |  作用        |
| ------------- |-------------|-------------|
| alpha | number | 透明度，0-1 |
| rgb | array | rgb颜色值，例如：[125, 255, 0] |

## 方法
| 方法名 | 作用 |
| ------------- |-------------|
| [toString](toString.md) | 转换为字符串描述 |
| [toNumber](toNumber.md) | 转换为整数描述 |
