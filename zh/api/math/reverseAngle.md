# [qc.Math](README.md).reverseAngle

## 原型
* number reverseAngle(angleRad)

## 参数说明
| 参数名 | 类型 | 说明 |
| ------------- | ------------- | -------------|
| angleRad | number | 弧度值 |
| 返回值 | number | 相反弧度值 |

## 说明
取弧度加PI后的规范弧度值

## 范例
````
    // 返回 0
    var ret = game.math.reverseAngle(Math.PI);

    // 返回 Math.PI
    var ret = game.math.reverseAngle(0);
````
