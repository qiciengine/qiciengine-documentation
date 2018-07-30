# NodeMask
The qc.NodeMask component is used to clip node's children.

````javascript
nodeMask = node.addScript('qc.NodeMask');
````

## Clip Mode  
1. __Rectangle：__ Only the content inside the node's bounds will be displayed.
````javascript
nodeMask.mode = qc.NodeMask.MODE_DEFAULT;
````

2. __Pixel：__ Use a texture for mask, only the content inside the opaque area of the texture will be displayed.
````javascript
nodeMask.mode = qc.NodeMask.MODE_PIXEL;
````

|Rectangle|Pixel(Circle)|
|:-----:|:-----:|
|![](images/mask1.png)|![](images/mask2.png)|

## Pixel Sample
1. Create two UIImage object, one as parent 'QICI', another one as child 'Sun'
2. Add "UI/NodeMask" component on the parent node
3. Set the "Clip Mode" as "Pixel" in Inspepctor panel
![](images/mask.png)

## Demo
[NodeMask](http://engine.qiciengine.com/demo/index.html#anchor_Mask)
