# Debug Viewer

The qc.DebugViewer component can be add on UIText or Dom node for displaying fps and time consumption information. 

![](images/debug_viewer.png)  
* __FPS__ - Frames per second
* __Draw Calls__ - Draw calls count, only valid in WebGL mode
* __Total__ - Total millisecond consumed every frame (Logic + Render)
* __Logic__ - The millisecond consumed of logical scripts every frame(PreUpdate + Update + postUpdate)
* __Render__ - The millisecond consumed for rendering

````javascript
nodeMask = text.addScript('qc.DebugViewer');
````

## Inspector Panel
![](images/debug_inspector.png)  
* __Debug On：__  If checked, the trace information will be output in console
* __Duration：__  The statistics interval by second

## Demo
[DebugView](http://engine.zuoyouxi.com/demo/index.html#Debug)
