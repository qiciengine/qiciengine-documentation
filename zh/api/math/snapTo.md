# [qc.Math](README.md).snapTo

## 原型
* number snapTo(input, gap, start)

## 参数说明
| 参数名 | 类型 | 说明 |
| ------------- | ------------- | -------------|
| input | number | 输入值 |
| gap | number | 间隔值 |
| start | number | 初值 |
| 返回值 | number |  |

## 说明
以指定间隔数进行四舍五入

## 范例
````
    // 返回 10
    var ret = game.math.snapTo(12, 5, 0);

    // 返回 15
    var ret = game.math.snapTo(13, 5, 0);
````
