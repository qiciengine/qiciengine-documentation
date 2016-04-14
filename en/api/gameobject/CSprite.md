# qc.Sprite
inherit [qc.Node](CNode.md)

## Description
Represents a Sprite object for use in 2D gameplay.
Sprites are 2D graphic objects used for characters, props, projectiles and other elments of 2D gameplay. The graphics are obtained from bitmap images.

The FrameAnimation and DragonBone are supported.

## Create a `Sprite`
````
var sprite = new qc.game.add.sprite(parent);
````

## Variables
|   Variable Name      |   Type       |  Description           |
| ------------- |-------------|-------------|
| animationNameList | array  |  Read only. The list of animation names. |
| animationType |  enum  |   Read only. The type of Animation: Sprite.NONE_ANIMATION, Sprite.FRAME_ANIMATION, Sprite.DRAGON_BONES, Sprite.FRAME_SAMPLES |
| defaultAnimation |  string  | The default animation' name. It will automatic play when awake. |
| armature | dragonBones.Armature | current armature node |
| frame | string | The frame' name in the texture atlas. |
| colorTint | [qc.Color](../color/README.md) | Get or set tint color. |
| isPlaying | bool | Read only. Is the sprite playing an animation? |
| isComplete | bool |  Read only. Is the animation is finished? |
| lastAnimationName | string | Read only. Last animation name played. |
| nativeSize | qc.Rectangle | The texture's real size. |
| paused | bool | Pause / Resume playing animation. |
| texture | qc.Texture | The texture atlas. |

## Events
|   Event      |     Description       |
| ------------- |-------------|
| onStart | When start playing animation, this event is trigged. |
| onFinished | When end playing animation, this event is trigged. |
| onLoopFinished | When play aimation in loop, this event is trigged when single loop is finished. |
| onTextureChanged | When texture change, this event is trigged. |

## Methods
| Method | Description |
| ------------- |-------------|
| [getAnimationInfo](sprite_getAnimationInfo.md) | Get the animation data. |
| [playAnimation](sprite_playAnimation.md) | Plays the animation. |
| [resetNativeSize](sprite_resetNativeSize.md) | Set the sprite' size to the texture's size. |
| [stop](sprite_stop.md) | Stop playing the animation. |

## Sample
````
bot = new game.add.sprite()
bot.x = 100;
bot.y = 200;
bot.texture = game.assets.find('bot');
bot.playAnimation('run', 1.5 /* Speed */, true /* Is Loop? */);
````

## Manual
[Sprite](http://docs.qiciengine.com/manual/Sample/Sprite.html)