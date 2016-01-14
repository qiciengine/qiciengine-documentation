# [qc.Math](README.md).smoothDamp

## Prototype
* array smoothDamp(current, target, currentVelocity, smoothTime, maxSpeed, deltaTime)

## Paramters
| Paramter | Type | Description |
| ------------- | ------------- | -------------|
| current | number | Current value |
| target | number | Target value |
| currentVelocity | number | Current velocity |
| smoothTime | number | Smooth time |
| maxSpeed | number | Max speed |
| deltaTime | number | Delta time between two frames |
| return | array | [pos, velocity]|

## Description
Calculate value of smooth damping.
