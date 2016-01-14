# Tween

## 描述
Tween动画组件的基类

## 变量
| 变量名 | 类型 | 作用 |
| ------------- |-------------|-------------|
| playOnAwake | boolean | 创建时是否自动播放动作，默认为false |
| flag | string | 组件的标记。当一个对象挂载多个相同Tween组件时会有用 |
| style | int | 循环类型，有3个取值：Tween.STYLE_ONCE(执行一次)、Tween.STYLE_LOOP(循环播放动画)、Tween.STYLE_PINGPONG(来回播放动画) |
| curve | qc.BezierCurve | 动画曲线 |
| delay | number | 延迟开始播放动画的时间，单位为秒 |
| duration | number | 动作的持续时间，单位为秒 |
| tweenGroup | int  | Tween的动作编组 |

## 事件
| 事件名 | 描述 |
| ------------- |-------------|
| onStart | 动作开始播放 |
| onFinished | 动作播放结束 |
| onLoopFinished | 循环动作播放一次结束了 |

## 方法
| 方法名 | 作用 |
| ------------- |-------------|
| [playForward](../tween/playForward.md) | 开始播放 |
| [playGroupForward](../tween/playGroupForward.md) | 开始成组播放 |
| [playReverse](../tween/playReverse.md) | 反向播放 |
| [playGroupReverse](../tween/playGroupReverse.md) | 开始反向成组播放 |
| [stop](../tween/stop.md) | 停止动作播放 |
| [stopGroup](../tween/stopGroup.md) | 停止整组的播放 |
| [resetToBeginning](../tween/resetToBeginning.md) | 重置为开始播放的状态 |
| [resetGroupToBeginning](../tween/resetGroupToBeginning.md) | 将Tween组重置为开始播放的状态 |

## 参考手册
[Tween动画](http://docs.zuoyouxi.com/manual/Tween/index.html)