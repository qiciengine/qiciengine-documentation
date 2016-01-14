# [qc.Math](README.md).minSub

## 原型
* number minSub(value, amount, min)

## 参数说明
| 参数名 | 类型 | 说明 |
| ------------- | ------------- | -------------|
| value | number | 值 |
| amount | number | 减值 |
| min | number | 最小值 |
| 返回值 | number |  |

## 说明
限制最小值的减法操作

## 范例
````
    // 返回 2
    var ret = game.math.minSub(3, 1, 1);

    // 返回 4
    var ret = game.math.minSub(3, 1, 4);
````
