# LayoutElement

## 描述
布局器使用的节点。用来控制节点在布局管理器中的表现。
尺寸分为：最小值，首选值，可变值，最大值。不设置时表示没有限制
满足规则如下：
 * 如果不能满足最小值的设定，则以最小值设置
 * 如果不能或者刚好满足首选值的设定，则以首选值为权重进行分配空间
 * 如果空间不大于最大值的设定，则将满足首选值外的剩余空间以可变值为权重进行分配
 * 如果大于最大值的设定，则按最大值设置

## 属性
| 变量名         |   类型      |  作用        |
| ------------- |-------------|-------------|
| ignoreLayout | bool | 是否允许忽略布局参数 |
| minWidth | int | 节点允许的最小宽度 |
| minHeight | int | 节点允许的最小高度 |
| preferredWidth | int | 首选宽度 |
| preferredHeight | int | 首选高度 |
| flexibleWidth | int | 可变宽度|
| flexibleHeight | int | 可变高度 |
| hasMinWidth | bool | 是否设置了最小宽度 |
| hasMinHeight | bool |是否设置了最小高度|
| hasPreferredWidth | bool | 是否设置了首选宽度|
| hasPreferredHeight | bool | 是否设置了首选高度 |
| hasFlexibleWidth | bool |是否设置了拓展宽度 |
| hasFlexibleHeight | bool | 是否设置了拓展高度 |

## 方法
| 方法名     |  作用        |
| ------------- |-------------|
| [getLayoutElement](layoutelement_getLayoutElement.md) | 获取一个节点上的布局元素 |
