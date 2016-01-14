# Graphics

qc.Graphics contains methods used to draw primitive shapes such as lines, circles and rectangles to display. This component need script to display content by calling drawing methods.

## API
* __drawTriangle__ Draw a single triangle  
* __drawTriangles__ Draw triangles  
* __lineStyle__ Specifies the line style   
* __moveTo__ Move the current drawing position  
* __lineTo__ Draw a line from current drawing point to the new point  
* __arcTo__ Creates an arc/curve between two tangents on the canvas.  
* __beginFill__ Specifies a simple one-color fill that subsequent calls to other drawing methods  
* __endFill__ Applies a fill to the lines and shapes that were added since the last call to the beginFill() method  
* __clear__ Clears the graphics that were drawn to this Graphics object, and resets fill and line style settings   
* __drawRect__ Draw a rectangle  
* __drawCircle__ Draw a circle  
* __drawEllipse__ Draws an ellipse  
* __drawPolygon__ Draws a polygon using the given path  
* __quadraticCurveTo__ Calculate the points for a quadratic bezier curve and then draws it  
* __bezierCurveTo__ Calculate the points for a bezier curve and then draws it   

## Video
<center>
<video controls="controls" src="../video/oper_graphics.mp4"></video>
</center>

## Demo
[Graphics Demo](http://engine.qiciengine.com/demo/Graphics/draw-line/index.html)

