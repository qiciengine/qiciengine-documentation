# qc.Device

## 描述
设备信息管理

## 变量
| 变量名 | 类型  | 作用 |
| ------------- |-------------|-------------|
| game | [qc.Game](../Game/README.md) | 游戏实例的引用 |
| desktop | boolean | 只读。当前是否运行在PC上 |
| iOS | boolean | 只读。当前是否运行在iOS设备上 |
| android | boolean | 只读。当前是否运行在android设备上 |
| webGL | boolean | 只读。当前是否支持WebGL加速 |
| vibration | boolean | 只读。当前设备是否支持震动 |
| browser | 枚举 | 只读。当前使用的浏览器，可以取如下值：Device.CHOME、Device.ARORA、Device.EPIPHANY、Device.FIREFOX、Device.TRIDENT、Device.IE、Device.MOBILE_SAFARI、Device.MODORI、Device.OPERA、Device.SAFARI、Device.SILK、Device.UCBROWSER、Device.UNKNOW |
| resolution | number | 只读。设备的分辨率 |
| fullscreen | boolean | 只读。是否支持全屏 |
| editor | boolean | 当前是否运行在editor模式下 |
| orientation | 枚举 | 当前设备处于横屏还是竖屏。可以取值：Device.AUTO、Device.PORTRAIT(Width < Height)、Device.LANDSCAPE(Width > Height) |

## 事件
| 事件名 | 作用 |
| ------------- |-------------|
| onOrientationChange | 屏幕分辨率的横竖屏发生变化时触发本事件。需要注意的是，我们使用的是游戏世界的宽度和高度来判断横竖屏 |

## Demo
[Device Demo](http://engine.zuoyouxi.com/demo/misc/device/index.html)