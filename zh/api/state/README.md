# qc.SceneManager

## 描述
游戏场景的管理器，负责场景的加载。可以通过game.scene访问本实例。

## 变量
| 变量名 | 类型 |作用 |
| ------------- |-------------|-------------|
| game | [qc.Game](../Game/README.md) | 游戏实例的引用 |
| entry | string | 游戏的入口场景名称 |
| list | object | 游戏的场景列表。key为场景名字，value为场景的资源路径(url) |
| loading | boolean | 当前是否正在加载场景中 |
| current | string | 当前运行中的场景名称 |

## 事件
| 事件名 | 作用 |
| ------------- |-------------|
| onStartLoad | 开始加载场景时，触发本事件 |
| onEndLoad | 场景加载完毕，触发本事件 |

## 方法
| 方法名 | 作用 |
| ------------- |-------------|
| [download](download.md) | 下载场景的资源 |
| [load](load.md) | 切换场景 |
