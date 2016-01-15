# [qc.Math](README.md).snapToCeil

## 原型
* number snapToCeil(input, gap, start)

## 参数说明
| 参数名 | 类型 | 说明 |
| ------------- | ------------- | -------------|
| input | number | 输入值 |
| gap | number | 间隔值 |
| start | number | 初值 |
| 返回值 | number |  |

## 说明
以指定间隔数向上取整

## 范例
````
    // 返回 15
    var ret = game.math.snapToCeil(11, 5, 0);

    // 返回 15
    var ret = game.math.snapToCeil(14, 5, 0);
````
