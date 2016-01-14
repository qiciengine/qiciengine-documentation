# HorizontalLayout and VerticalLayout
The qc.HorizontalLayout and qc.VerticalLayout inherit from qc.TableLayout, used for layouting children horizontally or vertically.

## Size Provider
See [TableLayout](TableLayout.html)

## Rule for calculating child node's size
The child node's size will be changed accroding to the settings:  

* ** Min width(height):** 0 by default
* ** Preferred width(height):** Uses the node's size or the native size for nine-patch image
* ** Extra width(height) ** 0 by default


1. If the node's width(height) is smaller than or equal to the sum of child node's min width(height), the child node's width(height) will be the min width(height).
````javascript
children[n].width = minWidth[n];
// or
children[n].height = minHeight[n];
````

2. If the node's width(height) is samller than or equal to the sum of the child node's preferred width(height), the extra part of the node's width(height) subtract the sum of the child node's min width(height), will be used to assign to the child node's width(height), basing on the weight that is calculated by the preferred width.
````javascript
children[n].width = minWidth[n] + (node.width - totalMinWidth) * preferredWidth[n] / totalPreferredWidth;
// or
children[n].height = minHeight[n] + (node.height - totalMinHeight) * preferredHeight[n] / totalPreferredHeight;
````

3. If the node's width(height) is bigger than the sum of the child node's preferred width(height), the extra part of the node's width(height) subtract the sum of the child node's preferred width(height), will be used to assign to the child node's width(height), basing on the weight that is calculated by the flexible width.
````javascript
children[n].width = preferredWidth[n] + (node.width - totalPreferredWidth) * flexibleWidth[n] / totalFlexibleWidth;
// or
children[n].height = preferredHeight[n] + (node.height - totalPreferredHeight) * flexibleHeight[n];
````
  
You can add [qc.LayoutElement][LayoutElement] component to the child node for customizing these settings.

## Content Align
Compare to [TableLayout][TableLayout], HorizontalLayout and VerticalLayout only provide the content align mode based on their direction.

### ** HorizontalLayout **
* ** Left: ** The left side of the table is align to the left side of the node
````javascript
tableLayout.contentAlignment = qc.TableLayout.ALIGN_TOP_LEFT;
````
* ** Center: ** The horizontal center of the table is align to the horizontal center of the node
````javascript
tableLayout.contentAlignment = qc.TableLayout.ALIGN_TOP_CENTER;
````
* ** Right: ** The right side of the table is align to the right side of the node
````javascript
tableLayout.contentAlignment = qc.TableLayout.ALIGN_TOP_RIGHT;
````

### ** VerticalLayout **
* ** Top: ** The top side of the table is align to the top side of the node
````javascript
tableLayout.contentAlignment = qc.TableLayout.ALIGN_TOP_LEFT;
````
* ** Middle: ** The vertical middle of the table is align to the vertical middle of the node  
````javascript
tableLayout.contentAlignment = qc.TableLayout.ALIGN_MIDDLE_LEFT;
````
* ** Bottom: ** The bottom side of the table is align to the bottom side of the node
````javascript
tableLayout.contentAlignment = qc.TableLayout.ALIGN_BOTTOM_LEFT;
````

## Cell Align
Compare to [TableLayout][TableLayout], HorizontalLayout and VerticalLayout only provide the cell align mode orthogonal to on their direction.
### ** HorizontalLayout **
* ** Top: ** The top side of the child node is align to the top of the cell
````javascript
tableLayout.contentAlignment = qc.TableLayout.ALIGN_TOP_LEFT;
````
* ** Middle: ** The vertical middle of the child node is align to the vertical middle of the cell  
````javascript
tableLayout.contentAlignment = qc.TableLayout.ALIGN_MIDDLE_LEFT;
````
* ** Bottom: ** The bottom side of the child node is align to the bottom of the cell
````javascript
tableLayout.contentAlignment = qc.TableLayout.ALIGN_BOTTOM_LEFT;
````

### ** VerticalLayout **
* ** Left: ** The left side of the child node is align to the left of the cell
````javascript
tableLayout.contentAlignment = qc.TableLayout.ALIGN_TOP_LEFT;
````
* ** Center: ** The horizontal center of the child node is align to the horizontal center of the cell  
````javascript
tableLayout.contentAlignment = qc.TableLayout.ALIGN_TOP_CENTER;
````
* ** Right: ** The right side of the child node is align to the right of the cell
````javascript
tableLayout.contentAlignment = qc.TableLayout.ALIGN_TOP_RIGHT;
````

### Force Expand
* **If the force direction is orthogonal to the layout, ** all the child node's width(height) will be the same with the node's width(height).

* **If the force direction is the same with the layout, ** all the child node's flexible width(height) will be set as 1 for layouting.

````javascript
tableLayout.childForceExpandWidth = true;
tableLayout.childForceExpandHeight = true;
````

## API
* [HorizontalLayout API](http://docs.qiciengine.com/api/components/HorizontalLayout.html)
* [VerticalLayout API](http://docs.qiciengine.com/api/components/VerticalLayout.html)
* [LayoutElement API][LayoutElement]

## Demo
[Demo](http://engine.qiciengine.com/demo/Layout/layout_horizontal/index.html)

