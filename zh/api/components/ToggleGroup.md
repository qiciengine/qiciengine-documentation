# ToggleGroup
见：[Toggle和ToggleGroup](http://docs.zuoyouxi.com/manual/Sample/Toggle.html)

## 描述
该组件在编辑器上加入 toggle 控件，用于管理多个 toggle 的开关切换

## 属性
| 变量名        |   类型       |  作用           |
| ------------- |-------------|-------------|
| toggle | qc.Toggle  |  当前处于激活状态的开关 |
| allowSwitchOff | boolean  |  是否允许选择为空 |
| toggles | array |  所有的开关列表 |
| onValueChange | qc.Signal |  开关组选中状态变化产生的事件 |