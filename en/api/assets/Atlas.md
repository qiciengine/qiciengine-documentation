# qc.Atlas

## Description
The class for atlas and animation.

## Variables
| Variable Name        | Type | Description           |
| ------------- |-------------|-------------|
| key | string | Read only. Unique asset key of the atlas file. |
| url | string | Read only. URL of the atlas file. |
| meta | object | Read only. Meta data of the atlas file. |
| animation | object | Read only. Animation information of the atlas file. |
| img | Image | Read only. The reference of the atlas image. |
| count | int | Read only. The number of frames. |
| frames | array | Read only. The list of frames. |
| frameNames | array | Read only. The name list of frames. |
| uuid | string |  Read only. The uuid of resource |

## Methods
| Method        | Description          |
| ------------- |-------------|
| [getFrame](atlas_getFrame.md) | Get a FrameData object from the atlas. |
| [getPadding](atlas_getPadding.md) | Get Nine-Patch information from the atlas. |

## Manual
[Texture Atlases](http://docs.qiciengine.com/manual/Atlas/index.html)
