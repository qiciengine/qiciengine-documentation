# [qc.Math](README.md).clamp

## 原型
* number clamp(x, min, max)

## 参数说明
| 参数名 | 类型 | 说明 |
| ------------- | ------------- | -------------|
| x | number | 值 |
| min | number | 最小值 |
| max | number | 最大值 |
| 返回值 | number |  |

## 说明
在 [min, max] 范围中取值，小于min，取 min，大于 max，取 max

## 范例
````
    // 返回 3
    var ret = game.math.clamp(3, 2, 4);

    // 返回 2
    var ret = game.math.clamp(1, 2, 4);

    // 返回 4
    var ret = game.math.clamp(5, 2, 4);
````
