# [qc.arcade.RigidBody](../RigidBody.md).moveToObject

## 原型
* void moveToObject(destination, speed, maxTime)

## 参数
| 参数名 | 类型 | 说明 |
| ------------- | ------------- | -------------|
| destination | object | 目标位置（需要包含x和y属性） |
| speed | number | 移动速度，每秒移动多少像素 |
| maxTime| number | 最大的耗时时间，单位毫秒 |

## 说明
按照一定的速度移动到目标位置，如果指定了maxTime，会自动调整移动速度（确保按照指定的时间到达目标点）。  
注意：移动时不会跟踪目标，且当移动到目标位置时不会停止。

