# [qc.Math](README.md).fuzzyGreaterThan

## 原型
* boolean fuzzyGreaterThan(a, b, epsilon)

## 参数说明
| 参数名 | 类型 | 说明 |
| ------------- | ------------- | -------------|
| a | number | 值 |
| b | number | 值 |
| epsilon | number | 精度值 |
| 返回值 | boolean | 在指定精度内，a 大于 b，返回 true |

## 说明
浮点数大于比较

## 范例
````
    // 返回 true
    var ret = game.math.fuzzyGreaterThan(1.232, 1.23, 0.00001);
````
