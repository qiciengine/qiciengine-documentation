# [qc.Math](README.md).wrap

## 原型
* number wrap(value, min, max)

## 参数说明
| 参数名 | 类型 | 说明 |
| ------------- | ------------- | -------------|
| value | number | 值 |
| min | number | 最小值 |
| max | number | 最大值 |
| 返回值 | number |  |

## 说明
取得一个 [min, max) 范围内的值
````
    var range = max - min;
    var result = (value - min) % range;
    if (result < 0)
    {
        result += range;
    }

    return result + min;
````

## 范例
````
    // 返回 8
    var ret = game.math.wrap(3, 5, 10);

    // 返回 9
    var ret = game.math.wrap(4, 5, 10);

    // 返回 9
    var ret = game.math.wrap(9, 5, 10);

    // 返回 6
    var ret = game.math.wrap(11, 5, 10);

    // 返回 7
    var ret = game.math.wrap(12, 5, 10);
````
