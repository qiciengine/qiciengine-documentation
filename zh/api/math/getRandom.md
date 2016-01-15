# [qc.Math](README.md).getRandom

## 原型
* number getRandom(objects, startIndex, length)

## 参数说明
| 参数名 | 类型 | 说明 |
| ------------- | ------------- | -------------|
| objects | array | 一组值 |
| startIndex | number | 初始索引，默认为0 |
| length | length | 默认为数组长度 |
| 返回值 | number | 返回数组中的随机元素 |

## 说明
从数组中取得一个随机元素

## 范例
````
    // 返回 3
    var ret = game.math.getRandom([3,4,2,5,9]);

    // 返回 5
    var ret = game.math.getRandom([3,4,2,5,9]);
````
