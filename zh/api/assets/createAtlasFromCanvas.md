# [qc.AssetUtil](AssetUtil.md).createAtlasFromCanvas

## 原型
* void createAtlasFromCanvas(game, key, canvas)

## 参数说明
| 参数名 | 类型 | 说明 |
| ------------- | ------------- | -------------|
| game | qc.Game | 游戏实例 |
| key | string | qc.Atlas 的 key |
| canvas | Canvas | 需要转成 qc.Atlas 的 Canvas 对象 |

## 说明
若指定 key 的 atlas 存在，且 canvas 一致，则将 texture 设为 dirty，直接返回该 atlas。 


