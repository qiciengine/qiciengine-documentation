# [qc.arcade.RigidBody](../RigidBody.md).moveToObject

## Prototype
* void moveToObject(destination, speed, maxTime)

## Parameters
| Parameter | Type | Description |
| ------------- | ------------- | -------------|
| destination | object | The display object to move. |
| speed | number | The speed it will move, in pixels per second. |
| maxTime| number | Time given in milliseconds. If set the speed is adjusted so the object will arrive at destination in the given number of ms. |

## Description
Move to an object through a specified speed.  
Note: The display object does not continuously track the target. If the target changes location during transit the display object will not modify its course.  
Note: The display object doesn't stop moving once it reaches the destination coordinates.

