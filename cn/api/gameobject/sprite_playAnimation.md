# [qc.Sprite](CSprite.md).playAnimation
函数

## 原型
* void playAnimation(string animationName, float speed, bool loop)

## 参数
| 参数名 | 类型 |  说明 |
| --------- | --------- | --------- |
| animationName | string |  动作名 |
| speed | float | 加速倍率，默认值：1.0（不加速） |
| loop | bool | 是否循环播放（undefined下则不干预，使用动作文件预设的loop进行播放）|

## 描述
播放一组动作。

## 示例
````
    sprite.playAnimation('attack');
````
