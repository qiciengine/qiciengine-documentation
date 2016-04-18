# TableLayout

## Description
A component for table layout.

## Variables
| Variable Name   |   Type      |  Description        |
| ------------- |-------------|-------------|
| constraint | int | Layout constraint, see [Constant](#_4) |
| startCorner | int | Layout start corner, left top by default |
| startAxis | int | Layout start direction, horizontal by default |
| contentSizeProvider | int | Size calculate mode. see[Bounds](Bounds.md)'s sizeProvider |
| style | int | Current layout style. TableLayout.STYLE_WRAP_ELEMENT、TableLayout.STYLE_RESIZE_ELEMENT. see [Constant](#_4)|
| spacingX | int | Spacing in x axis |
| spacingY | int | Spacing in y axis |
| cellWidth | int | Width of cell|
| cellHeight | int | Height of cell |
| contentAlignment | int | Alignment mode of content, effective only while style is TableLayout.STYLE_RESIZE_ELEMENT. |
| cellAlignment | int | Alignment mode of cell |
| columnsCount | int | Read Only. current column count |
| rowsCount | int |  Read Only. current row count |
| ignoreX | bool | Whether ignore the adjustment on the x-axis direction. |
| ignoreY | boo | Whether ignore the adjustment on the y-axis direction. |
| autoUpdate | bool | Whether relayout per frame automatically. |

## Methods
| Method        | Description          |
| ------------- |-------------|
| [getCellStyle](tablelayout_getCellStyle.md) | Get style of a cell |
| [setCellStyle](tablelayout_setCellStyle.md) | Set style of a cell |
| [clearCellStyle](tablelayout_clearCellStyle.md) | Clear style of a cell |
| [relayout](tablelayout_relayout.md) | Relayout container |
| [getCellRect](tablelayout_getCellRect.md) | Get box size of cell |
| [getCellLayout](tablelayout_getCellLayout.md) | Get layout of a cell |

## Constant
| Constant         |   Value      |  Description        |
| ------------- |-------------|-------------|
| TableLayout.CONSTRAINT_FLEXIBLE | Not limit row and column,automally adjust row and column by size  |
| TableLayout.CONSTRAINT_FIX_COLUMN_COUNT | Fixed column count  |
| TableLayout.CONSTRAINT_FIX_ROW_COUNT | Fixed row count  |
| TableLayout.STYLE_WRAP_ELEMENT | Keep cell size to layout.  |
| TableLayout.STYLE_RESIZE_ELEMENT | Keep self's RectTransform to layout, will change the size of cell  |
| TableLayout.AXIS_HORIZONTAL |  Horizontal direction    |
| TableLayout.AXIS_VERTICAL | Vertical direction |
| TableLayout.CORNER_TOP_LEFT | Top left corner  |
| TableLayout.CORNER_TOP_RIGHT | Top right cornet  |
| TableLayout.CORNER_BOTTOM_RIGHT | Bottom right cornet  |
| TableLayout.CORNER_BOTTOM_LEFT | Bottom left cornet  |
| TableLayout.ALIGN_LEFT | Horizontal left  |
| TableLayout.ALIGN_CENTER | Horizontal center  |
| TableLayout.ALIGN_RIGHT | Horizontal right  |
| TableLayout.ALIGN_TOP | Vertical top  |
| TableLayout.ALIGN_MIDDLE | Vertical center  |
| TableLayout.ALIGN_BOTTOM | Vertical bottom  |
| TableLayout.ALIGN_TOP_LEFT | Top left  |
| TableLayout.ALIGN_TOP_CENTER | Top center  |
| TableLayout.ALIGN_TOP_RIGHT | Top right  |
| TableLayout.ALIGN_MIDDLE_LEFT | Middle left   |
| TableLayout.ALIGN_MIDDLE_CENTER |Middle center  |
| TableLayout.ALIGN_MIDDLE_RIGHT | Middle right |
| TableLayout.ALIGN_BOTTOM_LEFT | Bottom left  |
| TableLayout.ALIGN_BOTTOM_CENTER |Bottom center|
| TableLayout.ALIGN_BOTTOM_RIGHT | Bottom right  |

## Manual
[TableLayout](http://docs.qiciengine.com/manual/Sample/TableLayout.html)
