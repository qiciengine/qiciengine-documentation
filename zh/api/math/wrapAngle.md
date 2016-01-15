# [qc.Math](README.md).wrapAngle

## 原型
* number wrapValue(angle, radians)

## 参数说明
| 参数名 | 类型 | 说明 |
| ------------- | ------------- | -------------|
| angle | number | 角度或弧度值 |
| radians | boolean | angle是否为弧度值 |
| 返回值 | number |  |

## 说明
保证一个角度或弧度值在 [-180,180) 或 [-PI,PI) 之间
````
        return radians ? this.wrap(angle, -Math.PI, Math.PI) : this.wrap(angle, -180, 180);
````

## 范例
````
    // 返回 -10
    var ret = game.math.wrapAngle(350);
````
