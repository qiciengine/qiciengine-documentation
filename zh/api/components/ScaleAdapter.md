# qc.ScaleAdapter

## 描述
行为组件，用户自适应分辨率。

## 属性
| 变量名        |   类型       |  作用           |
| ------------- |-------------|-------------|
| target | [qc.Node](../gameobject/CNode.md)  |  行为的目标 |
| referenceResolution | qc.Point | 希望使用的分辨率  |
| manualType | int | 分辨率适应的缩放类型，详见[常量](#_3)定义 |
| fullTarget | boolean | 是否使内容填满 |

## 常量
| 常量名         |   值      |  作用        |
| ------------- |-------------|-------------|
| ScaleAdapter.NONE | 0 | 不进行缩放 |
| ScaleAdapter.MANUAL_HEIGHT | 1 | 基于高度进行缩放，缩放后，坐标系中目标区域的高度为referenceResolution.y |
| ScaleAdapter.MANUAL_WIDTH | 2 | 基于宽度进行缩放，缩放后，坐标系中目标区域的宽度为referenceResolution.x |
| ScaleAdapter.EXPAND | 3 | 以参考矩阵为基础进行缩放，使其刚好完全放置在目标区域中 |
| ScaleAdapter.SHRIKN | 4 | 以参考矩阵为基础进行缩放，使其刚好包围整个目标区域 |
| ScaleAdapter.FILL | 5 | 对宽高分别进行缩放，使得目标区域的分辨率为referenceResolution |

## 参考手册
[屏幕自适应](http://docs.zuoyouxi.com/manual/UI/AdapterResolution.html)