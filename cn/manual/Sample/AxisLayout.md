# 水平布局与垂直布局
水平布局(HorizontalLayout)和垂直布局(VerticalLayout)是从表格布局(TableLayout)中拓展出来的两种特列。用于对子节点进行水平或者垂直布局管理。

## 尺寸提供方式(SizeProvider)
这个属性与[表格布局][TableLayout]的意义相同。

## 子节点的大小计算规则
在这两种布局中，子节点的大小会根据设置进行变化。
布局器会对每个子节点生成一组默认值：

* ** 最小宽（高）度：** 默认为0。
* ** 最佳宽（高）度：** 默认为图形的实际数值，对于九宫格图形而言是原始图片的大小。
* ** 可拓展的宽（高）度： ** 默认为0.

** 在计算子节点的大小时，按以下规则进行计算： **
1. 当节点的宽（高）小于或者等于所有子节点最小宽（高）之和时，设置每个子节点的宽（高）的值为最小值。
````javascript
children[n].width = minWidth[n];
// 或者
children[n].height = minHeight[n];
````
2. 当节点的宽（高）小于或者等于所有子节点的最佳宽（高）之和时，将超出最小宽（高）之和的多余部分，以最佳宽（高）为权重进行分配。
````javascript
children[n].width = minWidth[n] + (node.width - totalMinWidth) * preferredWidth[n] / totalPreferredWidth;
// 或者
children[n].height = minHeight[n] + (node.height - totalMinHeight) * preferredHeight[n] / totalPreferredHeight;
````
3. 当节点的宽（高）大于所有子节点的最佳宽（高）之和时，将超出最佳宽（高）之和的多余部分，以可拓展的宽（高）为权重进行分配。
````javascript
children[n].width = preferredWidth[n] + (node.width - totalPreferredWidth) * flexibleWidth[n] / totalFlexibleWidth;
// 或者
children[n].height = preferredHeight[n] + (node.height - totalPreferredHeight) * flexibleHeight[n];
````
  
如果需要手动设置这些值，可以在子节点上添加[qc.LayoutElement][LayoutElement]脚本，来进行控制。

## 内容的对齐方式
相比[表格布局][TableLayout]，水平（垂直）布局，精简了内容对齐方式，只提供在当前布局方向上的对齐控制。
### ** 水平布局 **
* ** 左边缘对齐(Left): ** 表格的左边与节点范围的左边对齐。
````javascript
tableLayout.contentAlignment = qc.TableLayout.ALIGN_TOP_LEFT;
````
* ** 水平居中对齐(Center): ** 表格的水平中点与节点范围的水平中点对齐。
````javascript
tableLayout.contentAlignment = qc.TableLayout.ALIGN_TOP_CENTER;
````
* ** 右边缘对齐(Right): ** 表格的右边与节点范围的右边对齐。
````javascript
tableLayout.contentAlignment = qc.TableLayout.ALIGN_TOP_RIGHT;
````

### ** 垂直布局 **
* ** 上边缘对齐(Top): ** 表格的上边与节点范围的上边对齐。
````javascript
tableLayout.contentAlignment = qc.TableLayout.ALIGN_TOP_LEFT;
````
* ** 垂直居中对齐(Middle): ** 表格的垂直中点与节点范围的垂直中点对齐。
````javascript
tableLayout.contentAlignment = qc.TableLayout.ALIGN_MIDDLE_LEFT;
````
* ** 下边缘对齐(Bottom): ** 表格的下边与节点范围的下边对齐。
````javascript
tableLayout.contentAlignment = qc.TableLayout.ALIGN_BOTTOM_LEFT;
````

## 单元格的对齐方式
相比[表格布局][TableLayout]，水平（垂直）布局，精简了单元格对齐方式，只提供在当前布局方向的垂直相交方向上的对齐控制。
### ** 水平布局 **
* ** 上边缘对齐(Top): ** 子节点的上边与单元格范围的上边对齐。
````javascript
tableLayout.contentAlignment = qc.TableLayout.ALIGN_TOP_LEFT;
````
* ** 垂直居中对齐(Middle): ** 子节点的垂直中点与单元格范围的垂直中点对齐。
````javascript
tableLayout.contentAlignment = qc.TableLayout.ALIGN_MIDDLE_LEFT;
````
* ** 下边缘对齐(Bottom): ** 子节点的下边与单元格范围的下边对齐。
````javascript
tableLayout.contentAlignment = qc.TableLayout.ALIGN_BOTTOM_LEFT;
````

### ** 垂直布局 **
* ** 左边缘对齐(Left): ** 子节点的左边与单元格范围的左边对齐。
````javascript
tableLayout.contentAlignment = qc.TableLayout.ALIGN_TOP_LEFT;
````
* ** 水平居中对齐(Center): ** 子节点的水平中点与单元格范围的水平中点对齐。
````javascript
tableLayout.contentAlignment = qc.TableLayout.ALIGN_TOP_CENTER;
````
* ** 右边缘对齐(Right): ** 子节点的右边与单元格范围的右边对齐。
````javascript
tableLayout.contentAlignment = qc.TableLayout.ALIGN_TOP_RIGHT;
````

### 强制拓展设置
* **当强制拓展方向与布局方向垂直相交时，** 将所有子节点的宽（高）的值设置为本节点的宽（高）
* **当强制拓展方向与布局方向相同时，** 将所有子节点的默认的可拓展宽（高）设置为1，然后计算布局。

````javascript
tableLayout.childForceExpandWidth = true;
tableLayout.childForceExpandHeight = true;
````

## API
[HorizontalLayout API](http://docs.zuoyouxi.com/api/components/HorizontalLayout.html)
[VerticalLayout API](http://docs.zuoyouxi.com/api/components/VerticalLayout.html)
[LayoutElement API][LayoutElement]

## Demo
[Demo](http://engine.zuoyouxi.com/demo/Layout/layout_horizontal/index.html)

[TableLayout]: TableLayout.html
[LayoutElement]: http://docs.zuoyouxi.com/api/components/LayoutElement.html