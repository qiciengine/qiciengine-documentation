# qc.Action

## 描述
_动作剪辑_ 文件在游戏中对应的类，该类用于控制 _动作剪辑_ 的播放等操作。

## 变量
| 变量名             | 类型              | 作用               |
| -------------   | -------------   | -------------    |
| game            | qc.Game          | 游戏实例        |
| targetObject    | qc.Node  | 播放该动作的目标对象       |
| targetLocked    | boolean   | 目标对象是否锁定          |
| samples  | int       | 每秒的帧数      |
| duration | int | 动作单次播放的时长              |
| loop           | boolean          | 是否循环          |

## 事件
| 事件名             | 作用               |
| -------------   | -------------    |
| onFinished            |   动作播放完毕的事件      |
| onLoopFinished            |   循环过程中单次播放完毕事件      |

## 方法
| 方法名            | 作用            |
| -------------  | ------------- |
| [setData](setData.md)  | 设置动作指定属性的数据       |

## 参考手册
[Action](http://docs.zuoyouxi.com/manual/Action/ActionEditor.html)
