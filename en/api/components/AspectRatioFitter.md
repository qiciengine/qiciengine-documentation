# qc.AspectRatioFitter

## Description
Resizes a RectTransform to fit a specified aspect ratio.

## Variables
| Variable Name   |   Type      |  Description        |
| ------------- |-------------|-------------|
| mode | int | The mode to use to enforce the aspect ratio. See: [Constants](#_3) |
| ratio | number | The aspect ratio |

## Constants
| Name         |   Value      |  Description        |
| ------------- |-------------|-------------|
| AspectRatioFitter.NONE | 0 | The aspect ratio is not enforced. |
| AspectRatioFitter.WIDTH_CONTROLS_HEIGHT | 1 | Changes the height of the rectangle to match the aspect ratio. |
| AspectRatioFitter.HEIGHT_CONTROLS_WIDTH | 2 | Changes the width of the rectangle to match the aspect ratio. |
| AspectRatioFitter.FIT_IN_PARENT | 3 | Sizes the rectangle such that it's fully contained within the parent rectangle. |
| AspectRatioFitter.ENVELOPE_PARENT | 4 | Sizes the rectangle such that the parent rectangle is fully contained within. |

## Manual
[AspectRatioFitter](http://docs.qiciengine.com/manual/Sample/AspectRatioFitter.html)