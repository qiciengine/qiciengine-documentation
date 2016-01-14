# [qc.Math](README.md).smoothDamp

## 原型
* array smoothDamp(current, target, currentVelocity, smoothTime, maxSpeed, deltaTime)

## 参数说明
| 参数名 | 类型 | 说明 |
| ------------- | ------------- | -------------|
| current | number | 当前值 |
| target | number | 目标值 |
| currentVelocity | number | 当前速度 |
| smoothTime | number | 阻尼时间 |
| maxSpeed | number | 最大速度 |
| deltaTime | number | 上一帧到现在的时间 |
| 返回值 | array | [pos, velocity]|

## 说明
平滑阻尼，根据以上参数，返回 [pos, velocity] 表示此时的移动信息.
