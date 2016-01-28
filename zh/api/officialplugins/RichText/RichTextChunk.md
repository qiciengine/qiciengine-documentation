# 富文本结构块

## 描述
记录富文本解析后的结构。

## 变量
| 变量名         |   类型      |  作用        |
| ------------- |-------------|-------------|
| type | number | 模块的类型 |
| tag | string | 模块的标签 |
| parent | RichTextChunk | 模块所属的结构块 |
| source | string | 解析的原始文本 |
| attributes | Object | 模块的属性值集合 |
| subs | Array | 属于该模块的子模块 |
| inner | Object | 模块包含的内容，通过toString()获取文本 |
| outer | Object | 模块完整的描述内容，通过toString()获取文本 |

## 常量
| 常量名         |   类型      |  作用        |
| ------------- |-------------|-------------|
| RichTextChunk.TEXT | number | 表示本结构块为文本结构 |
| RichTextChunk.BLOCK | number |  表示本结构块为块结构，解析时不会直接产生该类型的结构 |
| RichTextChunk.SYMBOL | number | 符号标记的结构块 |