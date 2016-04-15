# qc.Dom
inherit [qc.Node](CNode.md)

## Description
Dom node, is a div. Because it does not need render each frame, it is very efficient. See [Dom](http://docs.qiciengine.com/manual/Sample/Dom.html)

## Variables
| Variable Name        |   Type       |  Description           |
| ------------- |-------------|-------------|
| div | object  |  div element |
| pos | enum| The pos of node. There are two values: qc.Dom.BACK(back layer); qc.Dom.FRONT(top layer) |
| innerHTML | string | innerHTML property of div |
| className | string | CSS class  |
| serializable | boolean | Is innerHTML information needs to be saved, the default value is true  |
| overflow | enum | Corresponding to style.overflow, possible values: auto, hidden, visible, scroll  |
| zIndex | int | Corresponding to style.zIndex,  element with greater zIndex is always in front of another element with lower zIndex. Can not be set to zero. |

## Events
|   Event      |     Description       |
| ------------- |-------------|
| onVisibleChange | When father or self's visual property  change, the event will be fired. |

## Manual
[Dom](http://docs.qiciengine.com/manual/Sample/Dom.html)