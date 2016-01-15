# [qc.Math](README.md).fuzzyCeil

## 原型
* number fuzzyCeil(val, epsilon)

## 参数说明
| 参数名 | 类型 | 说明 |
| ------------- | ------------- | -------------|
| val | number | 值 |
| epsilon | number | 精度值 |
| 返回值 | number | 在指定精度内，val 向上取整 |

## 说明
浮点数向上取整

## 范例
````
    // 返回 2
    var ret = game.math.fuzzyCeil(1.0001, 0.00001);

    // 返回 1
    var ret = game.math.fuzzyCeil(1.00000001, 0.00001);
````
