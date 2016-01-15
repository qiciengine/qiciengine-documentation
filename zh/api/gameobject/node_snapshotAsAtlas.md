# [qc.Node](CNode.md).snapshotAsAtlas

## 原型
* [qc.Atlas](../assets/Atlas.md) snapshotAsAtlas(string key, [qc.Rectangle](../geom/Rectangle.md) srcBounds, number dstWidth, number dstHeight, number resolution)

## 参数
| 参数名 | 类型 |  说明 |
| --------- | --------- | --------- |
| key | string | atlas key，后续可以用 assets.find 来获取到资源 |
| srcBounds | [qc.Rectangle](../geom/Rectangle.md) | 绘制源的绘制区域，默认当前 Node 自身在屏幕中的最终宽高 |
| dstWidth | number | 绘制目标的宽，默认为 srcBound 的宽 |
| dstHeight | number | 绘制目标的高，默认为 srcBound 的高 |
| resolution | number | 生成的截图的解析度，默认选择当前游戏的 resolution |

## 描述
将当前节点的内容截屏，得到一张 [qc.Atlas](../assets/Atlas.md) 对象。

## 示例
````
    // 将当前节点的内容存储在 snapshot001 这张 atlas 上
    node.snapshotAsAtlas('snapshot001');

    // 设置某 image 的贴图为 snapshot001
    img.texture = this.game.assets.find('snapshot001')
````
