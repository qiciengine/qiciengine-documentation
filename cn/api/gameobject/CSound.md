# qc.Sound
inherit [qc.Node](CNode.md)

## 描述
声音组件。

## 创建声音节点
````
var sound = new qc.game.add.sound(parent);
````
创建见：[qc.GameObjectFactory](GameObjectFactory.md)

## 属性
| 属性名        |   类型       |  作用           |
| ------------- |-------------|-------------|
| audio | [qc.SoundAsset](../assets/SoundAsset.md) | 声音源 |
| destroyWhenStop | bool | 播放完毕之后是否自动销毁 |
| loop | bool | 是否循环播放当前声音 |
| mute | bool | 静音 |
| playOnAwake | bool | 是否创建时自动播放 |
| volume | number | 音量, 0 - 1 |
| isPlaying | bool | 是否正在播放 |
| isPaused | bool | 是否暂停中 |

## 方法
| 方法名 | 作用 |
| ------------- |-------------|
| [pause](sound_pause.md) | 暂停声音 |
| [play](sound_play.md) | 播放声音 |
| [fadeIn](sound_fadeIn.md) | 淡入播放声音 |
| [resume](sound_resume.md) | 恢复声音 |
| [stop](sound_stop.md) | 停止声音 |
| [addMarker](sound_addMarker.md) | 添加播放标记 从指定位置播放 |
| [removeMarker](sound_removeMarker.md) | 移除播放标记 |

## 参考手册
[声音](http://docs.zuoyouxi.com/manual/Sound/index.html)