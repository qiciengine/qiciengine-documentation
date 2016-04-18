# qc.TableLayout

## 描述
为容器提供表格布局功能

## 属性
| 变量名         |   类型      |  作用        |
| ------------- |-------------|-------------|
| constraint | int | 表格元素布局限制，见本文下方的[常量](#_4) |
| startCorner | int | 布局开始的角，默认从左上开始 |
| startAxis | int | 布局开始添加的轴，默认优先填充水平方向 |
| contentSizeProvider | int | 内容尺寸提供器，见[Bounds](Bounds.md)中的sizeProvider |
| style | int | 当前布局器的样式，是保持子节点大小还是以本节点 RectTransform 对子节点进行调整，默认保持子节点尺寸|
| spacingX | int | 单元格的水平间距 |
| spacingY | int | 单元格的垂直间距 |
| cellWidth | int | 单元格的宽度|
| cellHeight | int | 单元格的高度|
| contentAlignment | int | 内容在容器中的对齐方式，仅在style为TableLayout.STYLE_RESIZE_ELEMENT时生效 |
| cellAlignment | int | 单元格的内容在容器中的对齐方式 |
| columnsCount | int | 只读，当前列数 |
| rowsCount | int | 只读，当前行数 |
| ignoreX | bool | 是否不调整 x 坐标 |
| ignoreY | boo | 是否不调整 y 坐标 |
| autoUpdate | bool | 是否每帧自动重排 |

## 方法
| 方法名     |  作用        |
| ------------- |-------------|
| [getCellStyle](tablelayout_getCellStyle.md) | 获取一个单元格的样式 |
| [setCellStyle](tablelayout_setCellStyle.md) | 设置一个单元格样式 |
| [clearCellStyle](tablelayout_clearCellStyle.md) | 清除一个单元格样式 |
| [relayout](tablelayout_relayout.md) | 重新布局 |
| [getCellRect](tablelayout_getCellRect.md) | 获取表格单元格的包围大小 |
| [getCellLayout](tablelayout_getCellLayout.md) | 获取一个节点上的布局元素 |

## 常量
| 常量名     |  作用        |
| ------------- |-------------|
| TableLayout.CONSTRAINT_FLEXIBLE | 不限制行数和列数，根据大小自动进行调整  |
| TableLayout.CONSTRAINT_FIX_COLUMN_COUNT | 限制列数  |
| TableLayout.CONSTRAINT_FIX_ROW_COUNT | 限制行数  |
| TableLayout.STYLE_WRAP_ELEMENT | 保持子节点尺寸的情况下进行布局，Bounds会随着子节点的变化而变化  |
| TableLayout.STYLE_RESIZE_ELEMENT | 保持本节点的RectTransform，改变子节点的尺寸进行布局   |
| TableLayout.AXIS_HORIZONTAL | 水平方向  |
| TableLayout.AXIS_VERTICAL | 垂直方向  |
| TableLayout.CORNER_TOP_LEFT | 左上角  |
| TableLayout.CORNER_TOP_RIGHT | 右上角  |
| TableLayout.CORNER_BOTTOM_RIGHT | 右下角  |
| TableLayout.CORNER_BOTTOM_LEFT | 左下角  |
| TableLayout.ALIGN_LEFT | 水平居左  |
| TableLayout.ALIGN_CENTER | 水平居中  |
| TableLayout.ALIGN_RIGHT | 水平居右  |
| TableLayout.ALIGN_TOP | 垂直居上  |
| TableLayout.ALIGN_MIDDLE | 垂直居中  |
| TableLayout.ALIGN_BOTTOM | 垂直居下  |
| TableLayout.ALIGN_TOP_LEFT | 左上  |
| TableLayout.ALIGN_TOP_CENTER | 中上  |
| TableLayout.ALIGN_TOP_RIGHT | 右上  |
| TableLayout.ALIGN_MIDDLE_LEFT | 左中  |
| TableLayout.ALIGN_MIDDLE_CENTER | 正中  |
| TableLayout.ALIGN_MIDDLE_RIGHT | 右中  |
| TableLayout.ALIGN_BOTTOM_LEFT | 左下  |
| TableLayout.ALIGN_BOTTOM_CENTER | 中下  |
| TableLayout.ALIGN_BOTTOM_RIGHT | 右下  |

## 参考手册
[TableLayout](http://docs.zuoyouxi.com/manual/Sample/TableLayout.html)