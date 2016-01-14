# [qc.Math](README.md).fuzzyEqual

## 原型
* boolean fuzzyEqual(a, b, epsilon)

## 参数说明
| 参数名 | 类型 | 说明 |
| ------------- | ------------- | -------------|
| a | number | 值 |
| b | number | 值 |
| epsilon | number | 精度值 |
| 返回值 | boolean | a 与 b 指定精度内相等返回 true |

## 说明
浮点数相等比较

## 范例
````
    // 返回 true
    var ret = game.math.fuzzyEqual(1.23, 1.23, 0.00001);
````
