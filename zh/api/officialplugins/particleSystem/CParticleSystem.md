# qc.ParticleSystem
inherit [qc.Node](../../gameobject/CNode.md)

## 描述
粒子系统节点，继承自[Node](../../gameobject/CNode.md)，提供粒子相关功能。

## 变量
| 变量名        |  类型     |   作用           |
| ------------- |-------------| -------------|
| texture | qc.Atlas | 粒子使用的图集 |
| frames | Array | 粒子图片数组，当设定了多张图片时，在发射时将随机选取一个 |
| zoneType | number | 发射区域，支持四种类型：Zone.POINT(点)、Zone.LINE(直线)、Zone.CIRCLE(圆)、Zone.RECTANGLE(矩形)  |
| zoneLength | number | 发射区域长度，仅当zoneType为Zone.LINE时起效 |
| zoneRotation | number | 发射区域旋转角度，仅当zoneType为Zone.LINE时起效 |
| zoneRadius | number | 发射区域半径，仅当zoneType为Zone.CIRCLE时起效 |
| zoneWidth | number | 发射区域宽度，仅当zoneType为Zone.RECTANGLE时起效 |
| zoneHeight | number | 发射区域高度，仅当zoneType为Zone.RECTANGEL时起效 |
| frequency | number | 发射频率，即多久发射一次粒子，单位为秒 |
| quantity | number | 每次发射的粒子数量 |
| repeat | number | 重复发射次数，-1表示循环发射 |
| delay | number | 发射延迟，单位为秒 |
| lifespan | Array | 粒子生命时长，单位为秒，在指定范围内随机取值 |
| angle | Array | 粒子发射角度，在指定范围内随机取值 |
| blendMode | number | 混合模式 |
| srcColorTint | qc.Color | 粒子初始颜色 |
| dstColorTint | qc.Color | 粒子目标颜色 |
| startAlpha | Array | 粒子初始透明度，在指定范围内随机取值 |
| startScale | Array | 粒子初始缩放，在指定范围内随机取值 |
| startRotation | Array | 粒子初始旋转，在指定范围内随机取值 |
| startVelocity | Array | 粒子初始速度，在指定范围内随机取值 |
| angularVelocity | Array | 粒子旋转角速度，在指定范围内随机取值 |
| gravity | qc.Point | 重力 |
| maxParticles | number | 最大粒子数量，当粒子数量超过此值时将停止发射粒子 |
| playOnAwake | boolean | 激活时是否自动开始发射粒子 |
| enableColorCurve | boolean | 是否开启颜色控制曲线 |
| colorCurve | qc.BezierCurve | 粒子颜色控制曲线，若将此项关闭则粒子颜色将在起始颜色和目标颜色之间线性变化 |
| enableAlphaCurve | boolean | 是否开启透明度控制曲线 |
| alphaCurve | qc.BezierCurve | 粒子透明度控制曲线 |
| enableScaleCurve | boolean | 是否开启缩放控制曲线 |
| scaleCurve | qc.BezierCurve | 粒子缩放控制曲线 |
| enableVelocityCurve | boolean | 是否开启速度控制曲线 |
| velocityCurve | qc.BezierCurve | 粒子速度控制曲线 |
| enableAngularVelocityCurve | boolean | 是否开启角速度控制曲线 |
| angularVelocityCurve | qc.BezierCurve | 粒子角速度控制曲线 |

## 方法
| 方法 | 描述 |
| ------------- |-------------|
| [start](methods/start.md) | 启动粒子系统，开始发射粒子 |
| [pause](methods/pause.md) | 暂停粒子系统 |
| [clear](methods/clear.md) | 清除所有已发射的粒子 |
| [reset](methods/reset.md) | 重置粒子发射器 |

## 参考手册
[粒子系统](http://docs.zuoyouxi.com/manual/Plugin/ParticleSystem/ParticleSystem.html)
