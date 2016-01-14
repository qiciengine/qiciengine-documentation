# [qc.Math](README.md).min

## 原型
* number min(n1,n2,...)
* number min([n1,n2,...])

## 参数说明
| 参数名 | 类型 | 说明 |
| ------------- | ------------- | -------------|
| n1... | number | 一组值 |
| [n1,n2,...] | array | 一组值 |
| 返回值 | number | 返回最小值 |

## 说明
取最小值

## 范例
````
    // 返回 -5
    var ret = game.math.min(1,2,-5,4);

    // 返回 -5
    var ret = game.math.min([1,2,-5,4]);
````
