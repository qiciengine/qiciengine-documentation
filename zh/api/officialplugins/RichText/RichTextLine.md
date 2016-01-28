# 富文本显示行

## 描述
富文本中一行的显示内容

## 变量
| 变量名           | 类型                         | 作用            |
| ------------- | -------------              | ------------- |
| section       | RichTextSection            | 富文本显示段        |
| isClosed      | boolean                    | 行是否关闭         |
| blocks        | Array                      | 属于本行的所有显示块    |
| rect          | {x, y, width, height}      | 行的显示范围信息      |
| margin        | {left, right, top, bottom} | 行显示的外边距       |
| offset        | number                     | 行对于显示段的附加偏移   |
| styles        | Array                      | 行内所有使用的显示风格   |
| elementCount  | number                     | 行内所有的显示单元的数量  |
| elementSpace  | number                     | 显示单元的间隔       |

## 方法
| 方法名            | 作用            |
| -------------  | ------------- |
| close          | 关闭行           |
| closeLastBlock | 关闭最后一个结构块     |
| getLastBlock   | 获取最后一个结构块     |
| getCurrBlock   | 获取当前可操作的结构块   |
| remainSpace    | 行剩余的可用长度      |
