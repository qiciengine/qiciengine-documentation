# qc.UIText
inherit [qc.Node](CNode.md)

## 描述
显示文本的组件。

## 创建 text
````
    // 创建一个 text 节点
    var text = new qc.game.add.text(parent);
````

## 变量
| 变量名        |   类型       |  作用           |
| ------------- |-------------|-------------|
| autoSize | bool | 是否自动根据文字内容的宽高调整 text 的宽高 |
| fontFamily | number | 字体类型，目前有：UIText.SYSTEMFONT（系统字体）、UIText.WEBFONT（自定义字体资源）、UIText.BITMAPFONT（自定义图片字体） |
| alignH | number | 水平对齐方式，目前有：UIText.LEFT（左对齐）、UIText.CENTER（居中对齐）、UIText.RIGHT（右对齐） |
| alignV | number | 垂直对齐方式，目前有：UIText.TOP（上对齐）、UIText.MIDDLE（居中对齐）、UIText.BOTTOM（下对齐） |
| font | string或[qcFont](../assets/Font.md) |  字体，fontFamily为SYSTEMFONT时font类型为string，值为字体名字；fontFamily为其他类型的时候，font为字体资源 |
| bold | bool | 字体是否加粗 |
| fontSize | number | 字体大小，单位为 px |
| colorTint | [qc.Color](../color/README.md) | 颜色混合 |
| color | [qc.Color](../color/README.md) | 字体颜色 |
| text | string | 文本内容 |
| lineSpacing | number | 行间距，单位是 px |
| wrap | bool | 是否换行显示 |
| overflow | bool | 定义内容溢出的行为：如果为 true 则裁切，否则不裁切 |
| pivotX | number | 节点自身的原点X位置，0到1 |
| pivotY | number | 节点自身的原点Y位置，0到1 |
| width | number | 获取或设置文本的宽度 |
| height | number | 获取或设置文本的高度 |
| gradient | bool | 是否开启渐变 |
| startColor | [qc.Color](../color/README.md) | 渐变开始的颜色 |
| endColor | [qc.Color](../color/README.md) | 渐变结束的颜色 |
| stroke | [qc.Color](../color/README.md) | 描边的颜色 |
| strokeThickness | number | 描边的宽度 |
| enableShadow | bool | 是否显示阴影 |
| shadowColor | [qc.Color](../color/README.md) | 阴影的颜色 |
| shadowBlur | number | 阴影的模糊程度 |
| shadowOffsetX | number | 阴影偏移量X |
| shadowOffsetY | number | 阴影偏移量Y |
| enableGlow | bool | 是否启用外发光 |
| glowColor | [qc.Color](../color/README.md) | 外发光的颜色 |
| glowBlur | number | 外发光模糊值 |
| nativeSize | [qc.Rectangle](../geom/Rectangle.md) | text实际大小 |

## 参考手册
[文本](http://docs.zuoyouxi.com/manual/Sample/UIText.html)