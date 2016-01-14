# [qc.Node](CNode.md).snapshotAsAtlas

## Prototype
* [qc.Atlas](../assets/Atlas.md) snapshotAsAtlas(string key, [qc.Rectangle](../geom/Rectangle.md) srcBounds, number dstWidth, number dstHeight, number resolution)

## Parameters
| Parameter | Type | Description |
| --------- | --------- | --------- |
| key | string | Atlas key.  |
| srcBounds | [qc.Rectangle](../geom/Rectangle.md) | Source's bound for snapshot, current node's bound by default. |
| dstWidth | number | Target's width, value is srcBounds.width by default. |
| dstHeight | number | Target's height, value is srcBounds.height by default. |
| resolution | number | World's resolution by default. |

## Description
Snapshot node, return [qc.Atlas](../assets/Atlas.md) object.

## Example
````
    node.snapshotAsAtlas('snapshot001');

    img.texture = this.game.assets.find('snapshot001')
````
