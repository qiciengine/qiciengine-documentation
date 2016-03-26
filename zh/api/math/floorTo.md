# [qc.Math](README.md).floorTo

## 原型
* number floorTo(value, place, base)

## 参数说明
| 参数名 | 类型 | 说明 |
| ------------- | ------------- | -------------|
| value | number | 输入值 |
| place | number | 位数 |
| base | number | 默认为 10 |
| 返回值 | number |  |

## 说明
指定位数向下取整

## 范例
````
    // 返回 200
    var ret = game.math.floorTo(285.7142, 2);

    // 返回 280
    var ret = game.math.floorTo(285.7142, 1);

    // 返回 285
    var ret = game.math.floorTo(285.7142, 0);

    / 返回 285.7
    var ret = game.math.floorTo(285.7162, -1);

    / 返回 285.71
    var ret = game.math.floorTo(285.7162, -2);
````
