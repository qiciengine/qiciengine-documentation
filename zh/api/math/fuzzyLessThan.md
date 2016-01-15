# [qc.Math](README.md).fuzzyLessThan

## 原型
* boolean fuzzyLessThan(a, b, epsilon)

## 参数说明
| 参数名 | 类型 | 说明 |
| ------------- | ------------- | -------------|
| a | number | 值 |
| b | number | 值 |
| epsilon | number | 精度值 |
| 返回值 | boolean | 在指定精度内，a 小于 b，返回 true |

## 说明
浮点数小于比较

## 范例
````
    // 返回 true
    var ret = game.math.fuzzyLessThan(1.22, 1.23, 0.00001);
````
