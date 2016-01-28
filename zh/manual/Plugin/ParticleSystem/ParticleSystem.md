# 粒子系统

青瓷引擎中的粒子系统可以用来制作烟雾、火焰、爆炸和各种大气效果（如雨雪等），借助粒子系统，通过少量的图片资源就可以模拟出上述各种复杂效果。

# 开启插件

粒子系统目前以内置插件的形式提供，需要通过菜单 插件->插件管理 打开插件管理面板，并勾选 Particle System 选项。  
![](images/enable_plugin.png)   

# 创建粒子系统

开启粒子系统插件后，通过菜单 游戏对象->粒子系统 即可在场景中添加一个粒子系统物体。  
![](images/add_particle_system.png)   

# 粒子系统查看面板
选中场景中的粒子系统物体，即可通过属性查看面板对粒子系统的各种属性进行设置和预览。  
![](images/inspector_main_module.png)    

| 属性 | 描述 |
| ------------- | ------------- |
| Texture | 粒子系统使用的图集，图集的创建方式见文档[打包图集](../../../Atlas/README.md)。 |
| Frames | 粒子系统使用的图片帧，如果指定了多张图片，在发射时将随机选取一个。 |
| Zone | 发射区域，支持点、线段、圆、矩形四种区域类型，发射区域决定了粒子的初始位置。 |
| Frequency | 发射频率，即多久发射一次粒子，以秒为单位。 |
| Quantity | 每次发射的粒子数量。 |
| Repeat | 重复发射次数，若设置为-1则表示循环发射。 |
| Delay | 发射延迟，以秒为单位。 |
| Lifespan | 每个粒子的生命时长，在指定范围内随机取值，以秒为单位。 |
| Angle | 粒子的发射角度，在指定范围内随机取值，用来控制粒子的发射方向。 |
| BlendMode | 粒子的混合模式，对应于Phaser.blendModes |
| SrcColorTint | 粒子初始颜色，即粒子刚发射时的颜色。 |
| DstColorTint | 粒子目标颜色，即粒子生命结束时的颜色。 |
| StartAlpha | 粒子初始透明度，在指定范围内随机取值。 |
| StartScale | 粒子初始缩放，在指定范围内随机取值。 |
| StartRotation | 粒子初始旋转，在指定范围内随机取值。 |
| StartVelocity | 粒子初始速度，在指定范围内随机取值。 |
| AngularVelocity | 粒子初始角速度，在指定范围内随机取值。 |
| Gravity | 粒子系统重力，通过设置重力的水平和垂直分量值，可以实现粒子向某个方向加速运动。 |
| MaxParticles | 最大粒子数量，当粒子数量超过此值时将暂停发射。 |
| PlayOnAwake | 粒子系统激活时是否自动开始发射，若设置为false，需要手动调用相关接口进行发射（具体请参考[API文档](http://docs.zuoyouxi.com/api/officialplugins/particleSystem/CParticleSystem.html)） |

# 粒子颜色控制模块   
![](images/inspector_color_module.png)    
开启此模块后，可以通过曲线控制粒子在生命周期内的颜色变化。若将此模块关闭，粒子颜色将在SrcColorTint和DstColorTint间线性变化。

# 粒子透明度控制模块  
![](images/inspector_alpha_module.png)   
开启此模块后，可以通过曲线控制粒子在生命周期内的透明度变化。  
注：若粒子的透明度保持不变，应该将此模块关闭，以减少粒子系统的性能开销。

# 粒子缩放控制模块  
![](images/inspector_scale_module.png)   
开启此模块后，可以通过曲线控制粒子在生命周期内的缩放变化。  
注：若粒子的缩放保持不变，应该将此模块关闭，以减少粒子系统的性能开销。

# 粒子速度控制模块  
![](images/inspector_velocity_module.png)   
开启此模块后，可以通过曲线控制粒子在生命周期内的速度变化。  
注：若粒子的速度保持不变，应该将此模块关闭，以减少粒子系统的性能开销。

# 粒子角速度控制模块  
![](images/inspector_angular_velocity_module.png)   
开启此模块后，可以控制粒子在生命周期内的角速度变化。  
注：若粒子的角速度保持不变，应该将此模块关闭，以减少粒子系统的性能开销。

## API
[ParticleSystem API](http://docs.zuoyouxi.com/api/officialplugins/particleSystem/CParticleSystem.html)

## Demo
[ParticleSystem Demos](http://engine.zuoyouxi.com/demo/index.html#anchor_ParticleSystem)  