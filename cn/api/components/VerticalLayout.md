# VerticalLayout
inherit [qc.TableLayout](TableLayout.md)

## 描述
为容器提供垂直布局功能。初始化 [qc.TableLayout](TableLayout.md) 的以下几个参数：
````
    this.style = qc.TableLayout.STYLE_RESIZE_ELEMENT;
    this.constraint = qc.TableLayout.CONSTRAINT_FIX_COLUMN_COUNT;
    this.contentSizeProvider = qc.TableLayout.USE_RECTTRANSFORM;
    this.stride = 1;
    this.startCorner = qc.TableLayout.CORNER_TOP_LEFT;
    this.startAxis = qc.TableLayout.AXIS_VERTICAL;
````

## 属性
| 变量名         |   类型      |  作用        |
| ------------- |-------------|-------------|
| spacing | int | y轴方向布局间距 |
| childForceExpandWidth | int | 是否强制拉伸宽度|
| childForceExpandHeight | int | 是否强制拉伸高度 |

## 方法
| 方法名     |  作用        |
| ------------- |-------------|
| [getCellLayout](VerticalLayout_getCellLayout.md) | 获取在某一节点的布局系数 |

## 参考手册
[TableLayout](http://docs.zuoyouxi.com/manual/Sample/TableLayout.html)