# qc.Atlas

## 描述
图集、动画资源描述。

## 变量
| 变量名        | 类型 | 作用           |
| ------------- |-------------|-------------|
| key | string | 只读。资源关键字 |
| url | string | 只读。资源的地址 |
| meta | object | 只读。资源的meta数据 |
| animation | object | 只读。图集包含的动作信息 |
| img | Image | 只读。图集对应的图片 |
| count | int | 只读。图集包含的子图片数量 |
| frames | array | 只读。子图片列表 |
| frameNames | array | 只读。子图片的名字列表 |
| uuid | string | 只读。资源的 uuid |

## 方法
| 方法名        | 作用           |
| ------------- |-------------|
| [getFrame](atlas_getFrame.md) | 取得图集下某个图片信息 |
| [getPadding](atlas_getPadding.md) | 取得某个图片的九宫格信息 |

## 参考手册
[打包图集](http://docs.zuoyouxi.com/manual/Atlas/index.html)
