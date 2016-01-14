# [qc.Math](README.md).shuffle

## 原型
* Array shuffle(Array)

## 参数说明
| 参数名 | 类型 | 说明 |
| ------------- | ------------- | -------------|
| array | Array | 原列表，注意 shuffle 之后该 array 本身也发生变化 |
| 返回值 | Array | 洗牌后的列表 |

## 说明
将 array 中的元素随机打乱

## 范例
````
    // 返回 [2, 6, 3, 5, 4, 1]
    var ret = game.math.shuffle([1, 2, 3, 4, 5, 6])

    // 返回 [6, 1, 2, 4, 3, 5]
    var ret = game.math.shuffle([1, 2, 3, 4, 5, 6])
````
