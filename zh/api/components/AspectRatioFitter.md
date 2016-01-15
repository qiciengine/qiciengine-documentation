# qc.AspectRatioFitter

## 描述
保证节点的宽度和高度保持固定的比例

## 属性
| 变量名         |   类型      |  作用        |
| ------------- |-------------|-------------|
| mode | int | 控制比例的方式，详见[常量](#_3)定义 |
| ratio | number | 长宽的比例 |

## 常量
| 常量名         |   值      |  作用        |
| ------------- |-------------|-------------|
| AspectRatioFitter.NONE | 0 | 无，不进行控制 |
| AspectRatioFitter.WIDTH_CONTROLS_HEIGHT | 1 | 宽决定高 |
| AspectRatioFitter.HEIGHT_CONTROLS_WIDTH | 2 | 高决定宽 |
| AspectRatioFitter.FIT_IN_PARENT | 3 | 适合父亲节点大小 |
| AspectRatioFitter.ENVELOPE_PARENT | 4 | 填满父亲节点大小 |

## 参考手册
[AspectRatioFitter](http://docs.zuoyouxi.com/manual/Sample/AspectRatioFitter.html)