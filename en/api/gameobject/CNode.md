# qc.Node

## Description
Base class for all entities in scenes.

## Create a `Node`
See: [qc.GameObjectFactory](GameObjectFactory.md)
````
var node = new qc.game.add.node(parent);
````

## Variables
|   Variable Name  |   Type    |    Description     |
| ------------- |-------------|-------------|
| uuid | string | Unique identity of the node. |
| name | string | The node's name. |
| ignoreDestroy | bool | Makes the object target not be destroyed automatically when loading a new scene. |
| alpha | number | The node's alpha: 0 - 1 |
| visible | bool | The visible state of the node. Non-visible nodes and all of their children are not rendered. |
| parent | [qc.Node](CNode.md) |  The parent of the node. |
| worldVisible | bool | Read only. Indicates if the node is globally visible. |
| mask | PIXI.Graphics | Set mask, must be PIXI.Graphics |
| children | Array | Read only. The list of the node' children. |
| colorTint | [qc.Color](../color/README.md) | The tint applied to the node. |
| scripts | Array | Read only. The list of the components that this node attacks. |

### RectTransform
|   Variable Name   |   Type   |    Description     |
| ------------- |-------------|-------------|
| x | number | X position of the transform relative to the parent transform. |
| y | number | Y position of the transform relative to the parent transform. |
| anchoredX | number | The x position of the pivot of this RectTransform relative to the anchor reference point. |
| anchoredY | number | The y position of the pivot of this RectTransform relative to the anchor reference point. |
| scaleX | number | The scale.x of the transform relative to the parent. |
| scaleY | number | The scale.y of the transform relative to the parent. |
| pivotX | number | The x normalized position in this RectTransform that it rotates around. |
| pivotY | number | The y normalized position in this RectTransform that it rotates around. |
| rotation | number | The rotation of the transform relative to the parent transform's rotation. |
| width | number | The width of node. |
| height | number | The height of node. |
| minAnchor | [qc.Point](../geom/Point.md) | Read only. The normalized position in the parent RectTransform that the lower left corner is anchored to. Call [setAnchor](node_setAnchor.md) to set minAnchor.|
| maxAnchor | [qc.Point](../geom/Point.md) | Read only. The normalized position in the parent RectTransform that the upper right corner is anchored to. Call [setAnchor](node_setAnchor.md) to set maxAnchor. |
| left | number | Distance left relative to the parent transform. |
| right | number | Distance right relative to the parent transform. |
| top | number | Distance top relative to the parent transform. |
| bottom | number | Distance bottom relative to the parent transform. |
| rect | [qc.Rectangle](../geom/Rectangle.md) | The calculated rectangle in the local space of the Transform. |
| worldTransform | [qc.Matrix](../geom/Matrix.md) | Current transform of the object based on world (parent) factors |
| localBounds | [qc.Rectangle](../geom/Rectangle.md) | Retrieves the local bounds of the node as a rectangle object |
| onRelayout | [qc.Signal](../signal/README.md) | When transform changed, this event is triggered. |

### Input
|   Variable Name   |   Type    |    Description     |
| ------------- |-------------|-------------|
| interactive | boolean | Can pick up mouse / touch events? |
| hitArea | [qc.Rectangle](../geom/Rectangle.md)，[qc.Rectangle](../geom/Ellipse.md)，null，undefined | This is the defined area that will pick up mouse / touch events. It is null by default. |
| onDown | [qc.Signal](../signal/README.md) | When pointer pressed, this event is triggered. |
| onUp | [qc.Signal](../signal/README.md) | When pointer released, this event is triggered. |
| onClick | [qc.Signal](../signal/README.md) | When the node is click, this event is triggered. |
| onDragStart | [qc.Signal](../signal/README.md) | When starting a drag operation, onDragStart is called.  |
| onDrag | [qc.Signal](../signal/README.md) | When dragging, onDrag is called. |
| onDragEnd | [qc.Signal](../signal/README.md) | When ending a drag operation, onDragEnd is called. |
| onDragDrop | [qc.Signal](../signal/README.md) | When dropped, onDragDrop is called. |
| onWheel | [qc.Signal](../signal/README.md) | When mouse wheels, onWheel is called. |
| onEnter | [qc.Signal](../signal/README.md) | When mouse enters, onEnter is called. |
| onExit | [qc.Signal](../signal/README.md) | When mouse exits, onExit is called. |

## Methods
| Method | Description |
| ------------- |-------------|
| [addScript](node_addScript.md) | Adds a component class named className to the game object. Call [qc.Behaviour#destroy](../behaviour/destroy.md) to destroy.) |
| [getScript](node_getScript.md) | Returns the component if the node has one attached, null if it doesn't. |
| [getScripts](node_getScripts.md) | Returns all components in the node.  |
| [isDescendantOf](node_isDescendantOf.md) | Is the child of node? |
| [addChild](node_addChild.md) | Add a child node. |
| [addChildAt](node_addChildAt.md) | Add a child to the node at a specified index. If the index is out of bounds an error will be thrown  |
| [swapChildren](node_swapChildren.md) | Swaps the position of 2 Display Objects within this node. |
| [getChildIndex](node_getChildIndex.md) | Return the index position of a child node instance. |
| [setChildIndex](node_setChildIndex.md) | Change the position of an existing child in the node. |
| [getChildAt](node_getChildAt.md) | Return the child at the specified index |
| [removeChild](node_removeChild.md) | Remove a child from the node. |
| [removeChildAt](node_removeChildAt.md) | Removes a child from the specified index position. |
| [removeChildren](node_removeChildren.md) | Removes all children from this node. |
| [destroy](node_destroy.md) |  Remove this node. The node will be removed from scene in next frame.  |
| [destroyImmediately](node_destroyImmediately.md) |  Destroys the node immediately. You are strongly recommended to use destroy instead.  |
| [find](node_find.md) |  Finds a game object by name and returns it. |
| [addListener](addListener.md) | Listen event hook, it will be removed automatically when object destroy. |
| [addListenerOnce](addListenerOnce.md) | Listen event hook once, it will be removed automatically when event trigged once. |
| [removeListener](removeListener.md) | Remove listener manually. |
| [snapshotAsAtlas](node_snapshotAsAtlas.md) | Snapshot a node, return a [qc.Atlas](../assets/Atlas.md) object.|
| [snapshotAsImage](node_snapshotAsImage.md) | Snapshot a node, return a dom Image object. |

### RectTransform
| Method | Description |
| ------------- |-------------|
| [getWorldPosition](node_getWorldPosition.md) | Get the world position of node. |
| [getWorldScale](node_getWorldScale.md) | Get the world scale of node. |
| [getWorldRotation](node_getWorldRotation.md) | Get the world rotation of node. |
| [switchParent](node_switchParent.md) | Change the node's parent and hold position. |
| [getWorldCorners](node_getWorldCorners.md) | Get the node's four corners relative to world position. |
| [getWorldBox](node_getWorldBox.md) | Get the node's bounding box relative to world position. |
| [getBoxIn](node_getBoxIn.md) | Get the node's bounding box relative to a specific node. |
| [rectContains](node_rectContains.md) | Check if a world position is in the rectangle area. |
| [toGlobal](node_toGlobal.md) | Convert local position to world position. |
| [toLocal](node_toLocal.md) | Convert world position to local position. |
| [setAnchor](node_setAnchor.md) | Set the distance of this rectangle relative to a specified edge of the parent rectangle, while also setting its size. |
| [setStretch](node_setStretch.md) | Makes the RectTransform calculated rect be a given size on the specified axis. |

## Manual
[Node](http://docs.qiciengine.com/manual/Sample/Node.html)