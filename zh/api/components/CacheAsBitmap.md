# CacheAsBitmap

## 描述
提升渲染效率的利器，特别是在canvas模式下。本组件将节点缓存为一张图片，每次渲染时直接拿此图片进行渲染。  
本逻辑组件可以只缓存单个节点，也可以缓存节点及其所有子孙节点为一张图片。  
__需要注意的是，当内容改变时，需要设置dirty属性以刷新缓存图片__

## 属性
| 变量名         |   类型      |  作用        |
| ------------- |-------------|-------------|
| cacheType | int | 缓存的类型，有两个取值：CacheAsBitmap.CACHE_FOR_SCREEN(为屏幕显示创建缓存)、CacheAsBitmap.CACHE_FOR_SELF(为自身显示创建缓存) |
| boundsType | int | 缓存的边界类型，有两个取值：CacheAsBitmap.BOUNDS_SELF(只缓存单个节点)、CacheAsBitmap.BOUNDS_ALL(缓存自己和子孙) |
| boundsInScreen | boolean | 是否限制缓存区域大小，默认为false |
| dirty | boolean | 是否需要更新缓存内容 |

## 参考手册
[CacheAsBitmap](http://docs.zuoyouxi.com/manual/BuildinComponents/CacheAsBitmap.html)
