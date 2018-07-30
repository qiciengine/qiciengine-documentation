# qc.arcade.RigidBody

## Description

A component that control the position of an object through physics simulation.

## Variables
| Variable         |   Type      |  Description        |
| ------------- |-------------|-------------|
| mass | number | The mass of the rigibody, when two rigidbodies collide their mass is used in the calculation to determine the exchange of velocity. |
| moves | boolean | Whether allow the physics system to move this rigidbody. |
| immovable | boolean | Whether this rigidbody will not receive any impacts from other rigidbodies. |
| collideWorldBounds | boolean | Should the rigidbody collide with the world bounds? |
| allowRotation | boolean | Allow this rigidbody to be rotated? |
| allowGravity | boolean | Allow this rigidbody to be influenced by gravity?  |
| bounce | [qc.Point](../../geom/Point.md) | The elasticity of the rigidbody when colliding, bounce.x/y = 1 means full rebound, bounce.x/y = 0.5 means 50% rebound velocity. |
| velocity | [qc.Point](../../geom/Point.md) | Velocity of the rigidbody. |
| maxVelocity | [qc.Point](../../geom/Point.md) | Max vilocity of the rigidbody. |
| acceleration | [qc.Point](../../geom/Point.md) | The rate of change of the velocity. |
| drag | [qc.Point](../../geom/Point.md) | The drag applied to the motion of the rigidbody. |
| gravity | [qc.Point](../../geom/Point.md) | The local gravity setting of the rigidbody. Defaults to x: 0, y: 0 |
| friction | [qc.Point](../../geom/Point.md) | The amount of movement that will occur if another rigidbody 'rides' this one. |
| angularVelocity | number | The rotation speed of the rigidbody. Measured in radians per second. |
| maxAngular | number | Max rotation speed of the rigidbody. |
| angularAcceleration | number | The rate of change of the angular velocity. |
| angularDrag | number | The drag applied to the rotation of the rigidbody. |
| checkCollision | object | Which directions collision is processed for this rigidbody. |
| ccdIterations | int | Number of discrete points for continuous collision detection, used to prevent fast moving objects from passing through other objects without detecting collisions. Higher ccdIterations value means better physical collision, however the greater performance overhead. |
| collides | array | The rigidbodies used to collision detection. |
| overlaps | array | The rigidbodies used to overlap detection. |


## Methods
| Method | Description |
| ------------- |-------------|
| [reset](rigidbody/reset.md) | Reset the data of rigidbody. |
| [addCollide](rigidbody/addCollide.md) | Add a node for collision detection. |
| [removeCollide](rigidbody/removeCollide.md) | Remove a node for collision detection. |
| [addOverlap](rigidbody/addOverlap.md) | Add a node for overlap detection. |
| [removeOverlap](rigidbody/removeOverlap.md) | Remove a node for overlap detection. |
| [moveToObject](rigidbody/moveToObject.md) | Move to an object through a specified speed. |
| [velocityFromAngle](rigidbody/velocityFromAngle.md) | Get the velocity as a Point object through the angle (in degrees) and speed. |
| [velocityFromRotation](rigidbody/velocityFromRotation.md) | Get the velocity as a Point object through the rotation (in radians) and speed. |
| [accelerateToObject](rigidbody/accelerateToObject.md) | Move to an object through a specified acceleration.|
| [distanceBetween](rigidbody/distanceBetween.md) | Get the distance between two objects. |
| [angleBetween](rigidbody/angleBetween.md) | Get the angle(in radians) between to objects. |

## Manual
[RigidBody](http://docs.qiciengine.com/manual/Plugin/Arcade.html)
