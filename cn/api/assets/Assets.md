# qc.Assets

## 描述
负责游戏资源的加载、释放等。通过game.assets访问本实例，资源包含以下类型：
* [Atlas：图集、动画](Atlas.md)
* [ExcelAsset：Excel数据表](ExcelAsset.md)
* [Prefab：预制](Prefab.md)
* [SoundAsset：声音](SoundAsset.md)
* [TextAsset：文本](TextAsset.md)
* [Font：字体资源](Font.md)

## 变量
| 变量名        | 类型   | 描述           |
| ------------- |-------------|-------------|
| game | [qc.Game](../Game/README.md) | 游戏实例的引用 |
| isLoading | boolean | 只读。当前是否正在加载资源 |
| hasLoaded | boolean | 只读。所有资源是否已经加载解析完毕 |
| baseURL | string | 资源的域地址，所有的资源将附加本url头部 |
| parsing | boolean | 只读。当前是否有资源正在解析中 |
| loaded | int | 只读。已经加载完毕的资源数量 |
| total | int | 只读。需要加载的总资源数量 |
| maxRetryTimes | int | 资源加载失败的重试次数（重试间隔为1秒），默认：1 |

## 方法
| 方法名 | 作用 |
| ------------- |-------------|
| [load](load.md) | 请求异步加载资源 |
| [loadBatch](loadBatch.md) | 批量加载资源 |
| [find](find.md) | 查找资源 |
| [unload](unload.md) | 释放资源 |
| [clear](clear.md) | 清理所有资源 |
| [loadTexture](loadTexture.md) | 加载原始的图片资源（非打包资源） |

## 参考手册
[资源管理](http://docs.zuoyouxi.com/manual/AssetsLoad/index.html)
