# 富文本绘制风格

## 描述
用来管理绘制风格

## 变量
| 变量名                   | 类型            | 作用            |
| -------------         | ------------- | ------------- |
| font                  | string        | 字体            |
| fontSize              | number        | 字体大小          |
| fontWeight            | string        | 字体粗细          |
| fontStyle             | string        | 字体风格          |
| fontVariant           | string        | 字体变种          |
| cssFont               | string        | 当前使用css字体描述   |
| fontColor             | string        | 字体使用的颜色       |
| drawStyle             | string        | 绘制方式          |
| textAlign             | string        | 文本行的对齐方式      |
| verticalAlign         | string        | 文本在行内的对齐方式    |
| lineSpace             | number        | 行间距           |
| charSpace             | number        | 字间距           |
| preDrawHandle         | function      | 绘制之前的调用       |
| preDrawElementHandle  | function      | 绘制元素之前的调用     |
| drawElementHandle     | function      | 绘制元素的调用       |
| postDrawElementHandle | function      | 绘制元素之后的调用     |
| postDrawHandle        | function      | 绘制之后的调用       |
| onClickHandle         | function      | 元素被点击时的调用     |
| measureHandle         | function      | 计算元素显示属性的调用   |
	
## 方法
| 方法名           | 作用                                   |
| ------------- | -------------                        |
| getFont       | 获取字体描述                               |
| getFontHeight | 获取当前字体的高度                            |
| measureWord   | 计算单词的显示大小                            |
| measure       | 计算一个元素的显示大小                          |
| mixin         | 混合一个样式，整合所有非“_”开头的属性，并整合以handle结尾的方法 |
| preDraw       | 绘制之前的调用                              |
| drawElement   | 绘制元素                                 |
| postDraw      | 绘制之后的调用                              |
| onClick       | 使用该风格的元素被点击时的调用                      |

## 参考手册
[RichText](http://docs.zuoyouxi.com/manual/Plugin/RichText.html)
