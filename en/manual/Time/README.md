# Time System

In game you can manage time system through the code sample as below:  
````javascript
// Get the current system time
this.game.time.now;

// Set the game frame rate(frames per second)
this.game.time.frameRate = 60;

// Set time scale factor, 0.5 to make the game move fast
this.game.time.timeScale = 0.5;

// Add a new time event to be called after one second(the interval will be affected by the timeScale)
this.game.timer.add(1000, function() {
     // do something
});

// Add a new time event to be called every second(the interval will be affected by the timeScale)
this.game.timer.loop(1000, function() {
    // do something
});
````

## API and Demo
* [Time](http://docs.qiciengine.com/api/time/index.html)
* [Timer](http://docs.qiciengine.com/api/timer/index.html)
* [Demo](http://engine.qiciengine.com/demo/index.html#Time)
