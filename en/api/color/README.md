# qc.Color

## Description
The Color class is used to encapsulate colors in the default RGB color space

## Constructor
````
	// format: RRGGBB\AARRGGBB
	var c = new qc.Color('#ffffff');
	var c = new qc.Color('#FFFFFF');
	var c = new qc.Color('#CCFFFFFF');

	// format: RGB(red, green, blue)
	var c = new qc.Color('rgb(100, 125, 255)');
	var c = new qc.Color('RGB(100, 125, 255)');
	var c = new qc.Color('RGBA(100, 125, 255, 0.5)');
	var c = new qc.Color('rgba(100, 125, 255, 0.5)');

	// format: 0xRRGGBB
	var c = new qc.Color(0xffffff);

	// format: [red, green, blue, alpha]
	var c = new qc.Color([125, 100, 255]);
	var c = new qc.Color([125, 100, 255, 0.5]);
````

## Variables
| Variable Name         |   Type      |  Description        |
| ------------- |-------------|-------------|
| alpha | number | The alpha value defines the transparency of a color and can be represented by a float value in the range 0.0 - 1.0 |
| rgb | array | The value of rgb, such as: [125, 255, 0] |

## Methods
| Method | Description |
| ------------- |-------------|
| [toString](toString.md) | Convert a Color to string. |
| [toNumber](toNumber.md) | Convert a Color to int. |
