# [qc.Math](README.md).wrapValue

## 原型
* number wrapValue(value, amount, max)

## 参数说明
| 参数名 | 类型 | 说明 |
| ------------- | ------------- | -------------|
| value | number | 值 |
| amount | number | 加值 |
| max | number | 最大值 |
| 返回值 | number |  |

## 说明
两值相加后保证值在 [0,max) 范围内
````
        var diff;
        value = Math.abs(value);
        amount = Math.abs(amount);
        max = Math.abs(max);
        diff = (value + amount) % max;

        return diff;
````

## 范例
````
    // 返回 8
    var ret = game.math.wrapValue(3, 5, 10);

    // 返回 0
    var ret = game.math.wrapValue(5, 5, 10);

    // 返回 1
    var ret = game.math.wrapValue(6, 5, 10);
````
