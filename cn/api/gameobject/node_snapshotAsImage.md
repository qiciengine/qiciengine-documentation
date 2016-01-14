# [qc.Node](CNode.md).snapshotAsImage

## 原型
* Image snapshotAsImage([qc.Rectangle](../geom/Rectangle.md) srcBounds, number dstWidth, number dstHeight, number resolution, function loadedCallback)

## 参数
| 参数名 | 类型 |  说明 |
| --------- | --------- | --------- |
| srcBounds | [qc.Rectangle](../geom/Rectangle.md) | 绘制源的绘制区域，默认当前 Node 自身在屏幕中的最终宽高 |
| dstWidth | number | 绘制目标的宽，默认为 srcBound 的宽 |
| dstHeight | number | 绘制目标的高，默认为 srcBound 的高 |
| resolution | number | 生成的截图的解析度，默认选择当前游戏的 resolution |
| loadedCallback | function | image onload 之后的回调，可以不传入 |

## 描述
将当前节点的内容截屏，得到一个 Image 对象。

## 示例
````
    // 将当前节点的内容存储在一张 Image 中
    img = node.snapshotAsImage();

    // 添加到某个 div 中
    img.width = '100%';
    img.height = '100%';
    div.appendChild(img);
````
