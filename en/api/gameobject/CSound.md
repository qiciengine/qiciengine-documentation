# qc.Sound
inherit [qc.Node](CNode.md)

## Description
A representation of audio.

## Create a `Sound'
````
var sound = new qc.game.add.sound(parent);
````
See: [qc.GameObjectFactory](GameObjectFactory.md)

## Variables
| Variable Name       |   Type       |  Description           |
| ------------- |-------------|-------------|
| audio | [qc.SoundAsset](../assets/SoundAsset.md) | The asset of audio clip. |
| destroyWhenStop | bool | When the sound stop, destroy it. |
| loop | bool | Is the audio clip looping? |
| mute | bool | Un- / Mutes the Audio. |
| playOnAwake | bool | If set to be true, the sound will automatically start playing on awake. |
| volume | number | The volume of the audio (0.0 to 1.0). |
| isPlaying | bool | Whether is playing |
| isPaused | bool |  Whether is paused |

## Methods
| Method | Description |
| ------------- |-------------|
| [pause](sound_pause.md) | Pauses playing the clip. |
| [play](sound_play.md) | Plays the clip. |
| [fadeIn](sound_fadeIn.md) | Play sound in fadein mode |
| [resume](sound_resume.md) | Resumes playing the clip. |
| [stop](sound_stop.md) | Stops playing the clip. |
| [addMarker](sound_addMarker.md) | Add marker |
| [removeMarker](sound_removeMarker.md) | Remove marker |

## Manual
[Sound](http://docs.qiciengine.com/manual/Sound/index.html)