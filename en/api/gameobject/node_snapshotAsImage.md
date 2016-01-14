# [qc.Node](CNode.md).snapshotAsImage

## Prototype
* Image snapshotAsImage([qc.Rectangle](../geom/Rectangle.md) srcBounds, number dstWidth, number dstHeight, number resolution, function loadedCallback)

## Parameters
| Parameter | Type | Description |
| --------- | --------- | --------- |
| srcBounds | [qc.Rectangle](../geom/Rectangle.md) | Source's bound for snapshot, current node's bound by default. |
| dstWidth | number | Target's width, value is srcBounds.width by default. |
| dstHeight | number | Target's height, value is srcBounds.height by default. |
| resolution | number | World's resolution by default. |
| loadedCallback | function | Callback after image loaded. |

## Description
Snapshot node, return a dom Image object.

## Example
````
    img = node.snapshotAsImage();

    img.width = '100%';
    img.height = '100%';
    div.appendChild(img);
````
