# [qc.Math](README.md).roundTo

## 原型
* number roundTo(value, place, base)

## 参数说明
| 参数名 | 类型 | 说明 |
| ------------- | ------------- | -------------|
| value | number | 输入值 |
| place | number | 位数 |
| base | number | 默认为 10 |
| 返回值 | number |  |

## 说明
指定位数四舍五入

## 范例
````
    // 返回 300
    var ret = game.math.roundTo(285.7142, 2);

    // 返回 290
    var ret = game.math.roundTo(285.7142, 1);

    // 返回 286
    var ret = game.math.roundTo(285.7142, 0);

    / 返回 285.7
    var ret = game.math.roundTo(285.7162, -1);

    / 返回 285.72
    var ret = game.math.roundTo(285.7162, -2);
````
