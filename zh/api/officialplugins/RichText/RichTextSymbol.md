# 富文本符号注册管理

## 描述
用来管理和维护富文本中使用的符号和其表现

## 变量
| 变量名           | 类型            | 作用            |
| ------------- | ------------- | ------------- |
| game          | qc.Game       | 游戏实例          |


## 方法
| 方法名                           | 作用                              |
| -------------                 | -------------                   |
| registerSymbol                | 注册一个符号的处理，将覆盖已存在的处理方法。          |
| unregisterSymbol              | 移除一个符号的处理，如果有被覆盖的方法，则还原为原方法。    |
| getSymbolStyle                | 得到一份符号对应的绘制风格。                  |
| registerDrawStyle             | 注册一个绘制类型，将覆盖已存在的绘制类型。           |
| unregisterDrawStyle           | 移除一个绘制类型，如果有被覆盖的绘制方法，则还原为原绘制方法。 |
| getDrawStyle                  | 获取绘制类型对应的处理方法。                  |
| registerEmoji                 | 注册一个表情包                         |
| unregisterEmoji               | 移除一个表情包                         |
| findEmojiAtlas                | 获取一个表情对应的图集                     |
| registerToSystemSymbol        | 注册默认支持的符号                       |
| RichTextSymbol.doPostDrawText | 在文本绘制后马上进行下划线，删除线的绘制            |
| RichTextSymbol.fillText       | 填充方式的文本绘制                       |
| RichTextSymbol.strokeText     | 描边方式的文本绘制                       |

## 参考手册
[RichText](http://docs.zuoyouxi.com/manual/Plugin/RichText.html)