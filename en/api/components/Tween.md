# Tween

## Description
Base class for all tweening operations.

## Variables
| Variable Name | Type | Description |
| ------------- |-------------|-------------|
| playOnAwake | boolean | If set to be true, the tween will automatically start playing on awake. |
| flag | string | The flag of tween. |
| style | int | Does it play once? Does it loop? Value: Tween.STYLE_ONCE(Play Once)、Tween.STYLE_LOOP(Loop the tween)、Tween.STYLE_PINGPONG(Pingpong the tween) |
| curve | qc.BezierCurve | Curve of tween. |
| delay | number | How long will the tweener wait before starting the tween? Unit: second. |
| duration | number | How long is the duration of the tween? Unit: second. |
| tweenGroup | int  | Used by buttons and tween sequences. Group of '0' means not in a sequence. |

## Events
| Event | Description |
| ------------- |-------------|
| onStart | When the animation starts, this event is triggered. |
| onFinished | When the animation finishes, this event is triggered. |
| onLoopFinished | When the animation finishes a loop, this event is triggered. |

## Methods
| Method | Description |
| ------------- |-------------|
| [playForward](../tween/playForward.md) | Play the tween forward. |
| [playGroupForward](../tween/playGroupForward.md) | Play the tweens with same 'tweenGroup' forward. |
| [playReverse](../tween/playReverse.md) | Play the tween in reverse. |
| [playGroupReverse](../tween/playGroupReverse.md) | Play the tweens with same 'tweenGroup' in reverse. |
| [stop](../tween/stop.md) | Stop the tween. |
| [stopGroup](../tween/stopGroup.md) | Stop the tweens with same 'tweenGroup'. |
| [resetToBeginning](../tween/resetToBeginning.md) | Manually reset the tweener's state to the beginning. If the tween is playing forward, this means the tween's start. If the tween is playing in reverse, this means the tween's end. |
| [resetGroupToBeginning](../tween/resetGroupToBeginning.md) | Manually reset the tweener's state with same 'TweenGroup' to the beginning.  |

## Manual
[Tween Animation](http://docs.qiciengine.com/manual/Tween/index.html)