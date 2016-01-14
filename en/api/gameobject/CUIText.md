# qc.UIText
inherit [qc.Node](CNode.md)

## Description
The default Graphic to draw font data to screen.

## Create a `UIText`
````
    var text = new qc.game.add.text(parent);
````

## Variables
| Variable Name        |   Type       |  Description           |
| ------------- |-------------|-------------|
| autoSize | bool | Should the text be allowed to auto resized. |
| fontFamily | number | The FontType used by the text: UIText.SYSTEMFONT, UIText.WEBFONT, UIText.BITMAPFONT |
| alignH | enum | Horizontal alignment for text: UIText.LEFT, UIText.CENTER, UIText.RIGHT |
| alignV | enum | Vertical alignment for text: UIText.TOP, UIText.MIDDLE, UIText.BOTTOM |
| font | string or [qcFont](../assets/Font.md) |  When fontFamily is SYSTEMFONT, font is string type; fontFamily is other type，font is [qcFont](../assets/Font.md) |
| bold | bool | Bold style applied to your texts. |
| fontSize | number | The size that the Font should render at. |
| colorTint | [qc.Color](../color/README.md) | Tint color |
| color | [qc.Color](../color/README.md) | Base color of the font. |
| text | string | The string value this text will display. |
| lineSpacing | number | Line spacing, specified as a factor of font line height. A value of 1 will produce normal line spacing. |
| wrap | bool | Is the text can be wrap? |
| overflow | bool | Text flows freely outside the element. |
| pivotX | number | Rotations, size, and scale modifications occur around the pivot  |
| pivotY | number | Rotations, size, and scale modifications occur around the pivot  |
| width | number | The width of text |
| height | number |  The height of text |
| gradient | bool | Is the effect of gradient enabled? |
| startColor | [qc.Color](../color/README.md) | Start gradient color |
| endColor | [qc.Color](../color/README.md) | End gradient color |
| stroke | [qc.Color](../color/README.md) | Stroke color |
| strokeThickness | number | Stroke width |
| enableShadow | bool | Is the effect of shadow enable? |
| shadowColor | [qc.Color](../color/README.md) | The shadow's color. |
| shadowBlur | number | The shadow's blur. |
| shadowOffsetX | number | How far is the shadow from the text. |
| shadowOffsetY | number | How far is the shadow from the text. |
| enableGlow | bool | Is the effect of glow enable? |
| glowColor | [qc.Color](../color/README.md) | The glow's color. |
| glowBlur | number | The glow's blur. |
| nativeSize | [qc.Rectangle](../geom/Rectangle.md) | text real size |

## Manual
[UIText](http://docs.qiciengine.com/manual/Sample/UIText.html)