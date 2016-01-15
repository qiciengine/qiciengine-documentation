# [qc.Math](README.md).within

## 原型
* boolean within(a, b, tolerance)

## 参数说明
| 参数名 | 类型 | 说明 |
| ------------- | ------------- | -------------|
| a | number | 值 |
| b | number | 值 |
| tolerance | number | 范围 |
| 返回值 | boolean |  |

## 说明
判断两值相差的绝对值小于等于指定值
````
    return (Math.abs(a - b) <= tolerance);
````

## 范例
````
    // 返回 true
    var ret = game.math.within(3, 2, 2);
````
