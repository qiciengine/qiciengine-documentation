# qc.Device

## Description
Detects device support capabilities.  
This class represents a singleton object that can be accessed directly as `game.device`.  

## Variables
| Variable Name | Type  | Description |
| ------------- |-------------|-------------|
| game | [qc.Game](../game/README.md) | The local game reference. |
| desktop | boolean | Read only. Is running on a desktop? |
| iOS | boolean | Read only. Is running on iOS? |
| android | boolean | Read only. Is running on android? |
| webGL | boolean | Read only. Is webGL available? |
| vibration | boolean | Read only. Does the device support the Vibration API? |
| browser | enum | Read only. Can be: Device.CHOME, Device.ARORA, Device.EPIPHANY, Device.FIREFO, Device.TRIDENT, Device.IE, Device.MOBILE_SAFARI, Device.MODORI, Device.OPERA, Device.SAFARI, Device.SILK, Device.UCBROWSER, Device.UNKNOW |
| resolution | number | Read only. The device's resolution. |
| fullscreen | boolean | Read only. Does the browser support the Full Screen API? |
| editor | boolean | Is the game running in editor mode. |
| orientation | enum | The device's orientation. Value: Device.AUTO、Device.PORTRAIT(Width < Height)、Device.LANDSCAPE(Width > Height) |

## Events
| Event | Description |
| ------------- |-------------|
| onOrientationChange |  When the orientation changed, this event is triggered. |

## Demo
[Device Demo](http://engine.qiciengine.com/demo/misc/device/index.html)