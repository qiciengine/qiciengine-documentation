# [qc.Math](README.md).max

## 原型
* number max(n1,n2,...)
* number max([n1,n2,...])

## 参数说明
| 参数名 | 类型 | 说明 |
| ------------- | ------------- | -------------|
| n1... | number | 一组值 |
| [n1,n2,...] | array | 一组值 |
| 返回值 | number | 返回最大值 |

## 说明
取最大值

## 范例
````
    // 返回 4
    var ret = game.math.max(1,2,-5,4);

    // 返回 4
    var ret = game.math.max([1,2,-5,4]);
````
