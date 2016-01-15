# qc.Prefab

## 说明
预制资源。在编辑器中将场景对象拖入 Project 指定目录中，会自动创建预制资源，该预制资源保存了对象的信息，在加载预制
资源时，会自动创建 qc.Prefab 对象，然后可通过 [game.add.clone](../gameobject/clone.md) 克隆出预制对象
所保存的对象。

## 变量
| 变量名        | 类型 | 作用           |
| ------------- |-------------|-------------|
| uuid | string | 只读。资源的唯一标识符 |
| dependences | Array | 只读。预制依赖的资源列表 |

## 参考手册
[预制](http://docs.zuoyouxi.com/manual/Prefab/index.html)
