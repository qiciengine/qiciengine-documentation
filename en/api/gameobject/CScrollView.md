# qc.ScrollView
inherit [qc.Node](CNode.md)

## Description
Make a child RectTransform scroll.

## Create a `ScrollView`
````
var scrollView = new qc.game.add.scrollView(parent);
````

## Variables
| Variable Name     |  Type     |   Description           |
| ------------- |-------------| -------------|
| canHorizontal | bool | Should horizontal scrolling be enabled? |
| canVertical | bool | Should vertical scrolling be enabled? |
| movementType | enum | The behavior to use when the content moves beyond the scroll rect: ScrollView.MOVEMENT_UNRESTRICTED(Unrestricted movement. The content can move forever.), ScrollView.MOVEMENT_ELASTIC(Elastic movement. The content is allowed to temporarily move beyond the container, but is pulled back elastically.), ScrollView.MOVEMENT_CLAMPED(Clamped movement. The content can not be moved beyond its container.) |
| elasticity | number | The amount of elasticity to use when the content moves beyond the scroll rect. |
| inertia | bool | Should movement inertia be enabled? |
| decelerationRate | number | The rate at which movement slows down. |
| scrollSensitivity | number | The sensitivity to scroll wheel and track pad scroll events. |
| propagationScroll | bool | Whether the scroll event is passed to the upper. |
| content | [qc.Node](CNode.md） | The content that can be scrolled. It should be a child of this scrollView. |
| horizontalScrollBar | [qc.ScrollBar](CScrollBar.md) or null | Optional Scrollbar object linked to the horizontal scrolling of the ScrollView. |
| horizontalNormalizedPosition | number | The horizontal scroll position between 0 and 1. |
| verticalScrollBar | [qc.ScrollBar](CScrollBar.md) or null | Optional Scrollbar object linked to the vertical scrolling of the ScrollView. |
| verticalNormalizedPosition | number | The vertical scroll position between 0 and 1. |

## Methods
| Method | Description |
| ------------- |-------------|
| [setNormalizedPosition](sv_setNormalizedPosition.md) | Set the scroll position.  |

## Events
| Event  | Description |
| ------------- |-------------|
| onValueChange | When scrolling, this event is triggered. |

## Manual
[ScrollView](http://docs.qiciengine.com/manual/Sample/ScrollView.html)
