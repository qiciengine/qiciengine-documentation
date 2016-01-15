# [qc.Math](README.md).normalizeAngle

## 原型
* number normalizeAngle(angleRad)

## 参数说明
| 参数名 | 类型 | 说明 |
| ------------- | ------------- | -------------|
| angleRad | number | 弧度值 |
| 返回值 | number | [0,2pi)内弧度值 |

## 说明
 将弧度值规范为[0,2PI)的弧度

## 范例
````
    // 返回 Math.PI
    var ret = game.math.normalizeAngle(3 * Math.PI);
````
