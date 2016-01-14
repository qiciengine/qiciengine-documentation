# 着色器
__注意：着色器(Filter)只在支持WebGL的浏览器上有效果，在Canvas渲染模式下着色器的效果不起效。__

## 使用着色器

1. 添加 UI/FilterGroup 组件到UIImage节点  
![](images/filtergroup.png) 

2. 通过“Add Filter”按钮可以添加各着色器，一个UIImage可以有多个Filter来混合出各种组合效果。    
![](images/addfilters.png) 

## 着色器类型

目前提供的内置着色器支持如下效果：
    
1. __qc.Filter.AlphaMask__   
  ![](images/alphamask1.png)    
  ![](images/alphamask2.png)    
Other Texture: 采用另一张图片的透明度信息混合原始图片

2. __qc.Filter.Highlight__  
  ![](images/highlight1.png)        
  ![](images/highlight2.png)   
Light: 0~1，高亮因素     
Light Color: 高亮颜色   
      
3. __qc.Filter.BlurX__  
  ![](images/blurx1.png)        
  ![](images/blurx2.png)     
Blur: 水平模糊因素    
    
4. __qc.Filter.BlurY__   
  ![](images/blury1.png)        
  ![](images/blury2.png)     
Blur: 垂直模糊因素    
    
5. __qc.Filter.Gray__   
  ![](images/gray1.png)           
  ![](images/gray2.png)     

6. __qc.Filter.BlendTexture__   
  ![](images/blend1.png)           
  ![](images/blend2.png)     
Other Texture: 采用另一张图片的透明度信息混合原始图片    
Mix: 0~1，混合因素   
 
7. __qc.Filter.KeepSource__     
  ![](images/keepsource1.png)                  
  ![](images/keepsource2.png)     

## Demo
[Filter Demo](http://engine.zuoyouxi.com/demo/Filter/filter_mixed/index.html)     
