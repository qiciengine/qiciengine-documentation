# 时间系统

游戏内使用的时间管理、定时器管理等，可以通过如下代码访问：  
````javascript
// 当前的系统时间
this.game.time.now;

// 设定当前的游戏帧率
this.game.time.frameRate = 60;

// 游戏加速
this.game.time.timeScale = 0.5;

// 添加时间事件，一秒后回调，受timeScale影响
this.game.timer.add(1000, function() {
     // do something
});

// 添加时间事件，每秒回调一次，受timeScale影响
this.game.timer.loop(1000, function() {
    // do something
});
````

## API与范例
* [Time](http://docs.zuoyouxi.com/api/time/index.html)
* [Timer](http://docs.zuoyouxi.com/api/timer/index.html)
* [Demo](http://engine.zuoyouxi.com/demo/index.html#anchor_Time)
