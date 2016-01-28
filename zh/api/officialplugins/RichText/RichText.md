# 富文本组件

## 描述
用来在游戏世界中绘制富文本

## 变量
| 变量名             | 类型              | 作用               |
| -------------   | -------------   | -------------    |
| text            | string          | 用来显示的文本内容        |
| symbol          | RichTextSymbol  | 富文本使用的符号环境       |
| defaultStyle    | RichTextStyle   | 文本的默认样式          |
| richTextChunks  | Array           | 富文本解析出来的结构块      |
| richTextSection | RichTextSection | 显示段              |
| order           | number          | 文本的显示顺序          |
| wrap            | number          | 文本的自动换行模式        |
| font            | string          | 默认的文本字体          |
| fontSize        | number          | 默认的文本大小          |
| bold            | boolean         | 默认是否粗体           |
| italic          | boolean         | 默认是否斜体           |
| color           | string          | 默认显示颜色           |
| updateBounds    | boolean         | 是否根据文本显示区域更新节点大小 |

## 方法
| 方法名            | 作用            |
| -------------  | ------------- |
| rebuildChunks  | 重建富文本结构       |
| rebuildSection | 重建富文本显示段      |
| rebuildTexture | 重建绘制贴图        |

## 参考手册
[RichText](http://docs.zuoyouxi.com/manual/Plugin/RichText.html)