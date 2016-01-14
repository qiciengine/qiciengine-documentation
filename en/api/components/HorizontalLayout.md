# HorizontalLayout
inherit [qc.TableLayout](TableLayout.md)

## Description
Layout child layout elements side by side.

The HorizontalLayoutGroup component is used to layout child layout elements side by side according to their respective minimum, preferred, and flexible widths.

It initialize these following paras for [qc.TableLayout](TableLayout.md)
````
    this.style = qc.TableLayout.STYLE_RESIZE_ELEMENT;
    this.constraint = qc.TableLayout.CONSTRAINT_FIX_ROW_COUNT;
    this.contentSizeProvider = qc.TableLayout.USE_RECTTRANSFORM;
    this.stride = 1;
    this.startCorner = qc.TableLayout.CORNER_TOP_LEFT;
    this.startAxis = qc.TableLayout.AXIS_HORIZONTAL;
````

## Variables
| Variable Name   |   Type      |  Description        |
| ------------- |-------------|-------------|
| spacing | int | Spacing value |
| childForceExpandWidth | int | Whether to stretch width forcely |
| childForceExpandHeight | int | Whether to stretch height forcely|

## Methods
| Method        | Description          |
| ------------- |-------------|
| [getCellLayout](HorizontalLayout_getCellLayout.md) | Get the layout of a cell |

## Manual
[TableLayout](http://docs.qiciengine.com/manual/Sample/TableLayout.html)