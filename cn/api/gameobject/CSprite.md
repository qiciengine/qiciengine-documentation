# qc.Sprite
inherit [qc.Node](CNode.md)

## 描述
显示2D动画的组件，目前主要用于创建帧动画、Dragons骨骼动画。

## 创建 Sprite
````
var sprite = new qc.game.add.sprite(parent);
````

## 变量
| 变量名        |   类型       |  作用           |
| ------------- |-------------|-------------|
| animationNameList | array  |  只读，当前资源的动作名列表 |
| animationType |  number  |  只读，动画的类型（Sprite.NONE_ANIMATION，Sprite.FRAME_ANIMATION，Sprite.DRAGON_BONES，Sprite.FRAME_SAMPLES) |
| defaultAnimation |  string  | 默认的动作名称，反序列化将自动播放。 |
| armature | dragonBones.Armature | 获取当前使用的骨骼根节点 |
| frame | string | 具体的图片帧（播放动作中以及骨骼动画情况下，设置 frame 是无效的） |
| colorTint | [qc.Color](../color/README.md) | 设置颜色混合 |
| isPlaying | bool | 只读，动作是否在播放中 |
| isComplete | bool |  只读，动作是否结束 |
| lastAnimationName | string | 只读，上一个（如果正在播放中，则为当前）播放的动作名 |
| nativeSize | qc.Rectangle | 当前 Sprite 所用到的图片的原始大小 |
| paused | bool | 属性，动作是否暂停 && 设置暂停动作 |
| texture | qc.Atlas | 动画资源（qc.Atlas对象，可通过  game.assets.find(key) 来获取)，若有动画信息，则创建动画管理器 |

## 事件
|   事件名      |     作用       |
| ------------- |-------------|
| onStart | 动作开始播放的事件 |
| onFinished | 动作播放结束的事件 |
| onLoopFinished | 循环动作一轮播放结束的事件。当前 Sprite 播放某个动作多次的时候，除却最后一次播放结束（onFinished事件），中间的每轮播放结束都会发出一个 onLoopFinished 事件。 |
| onTextureChanged | 当显示的贴图发生变化时触发的事件 |

## 方法
| 方法名 | 作用 |
| ------------- |-------------|
| [getAnimationInfo](sprite_getAnimationInfo.md) | 获取某个动作的具体信息 |
| [playAnimation](sprite_playAnimation.md) | 开始播放动作 |
| [resetNativeSize](sprite_resetNativeSize.md) | 设置为图片原始的大小（图片不缩放） |
| [stop](sprite_stop.md) | 停止播放当前动作 |

## 示例
````
bot = new game.add.sprite()
bot.x = 100;
bot.y = 200;
bot.texture = game.assets.find('bot');
bot.playAnimation('run', 1.5 /* 倍率 */, true /* 循环 */);
````

## 参考手册
[精灵](http://docs.zuoyouxi.com/manual/Sample/Sprite.html)