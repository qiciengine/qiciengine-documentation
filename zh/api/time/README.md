# qc.Time

## 说明
游戏的时间系统，可以通过game.time访问本实例

## 变量
| 变量名        |  类型 | 描述           |
| ------------- |-------------|
| game | [qc.Game](../game/README.md) | 游戏实例的引用 |
| frameRate | int | 游戏帧率。 |
| now | int | 只读。现在的时间戳 (1970-01-01午夜到现在的时间间隔，用毫秒表述) |
| scaledTime  | int | 只读。自游戏开始后经历的时间，受timeScale加速的影响 |
| fixedTime | int | 只读。以毫秒秒计自游戏开始的时间 | 
| timeScale | number | 控制时间的快慢，默认为1。 |
| deltaTime | number | 只读。最后一帧到当前帧的时间间隔（单位：毫秒）|

## 方法
无

## 参考手册
[时间系统](http://docs.zuoyouxi.com/manual/Time/index.html)