# Dirty Rectangles

QICI Engine supports dirty rectangles management for canvas rendering, helping to avoid mobile device overheating and improve rendering performance.

## Enable Dirty Rectangles
There are two ways to enable the dirty rectangles management function:  
* In [Project Settings](../Settings/README.md) check "Dirty Rectangles" 
* Use code dynamically
````javascript
this.game.dirtyRectangle.enable = true;
````

## Show Dirty Rectangles 
There are three ways to show dirty rectangles at runtime:
* In [Project Settings](../Settings/README.md) check "Show Dirty Rectangles" 
* Use code dynamically
````javascript
game.dirtyRectangle.showDirtyRegion = true;
````
* Enable paint flashing from Google Chrome browser's debugging feature  
![](images/dirtyrectangles.png)  

## Force Redraw All
In some case you need to update the whole game screen, then you can use the code as below to force redraw all for the next frame.   
````javascript
this.game.dirtyRectangle.forceDirty = true;
````
