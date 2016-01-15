# qc.TransitionBehaviour

## 描述
行为组件，用于表现交互元素的状态：普通、按下、不可用。（例如 [qc.Button](../gameobject/CButton.md) 组件就具有该行为）

## 属性
| 变量名        |   类型       |  作用           |
| ------------- |-------------|-------------|
| target | [qc.Node](../gameobject/CNode.md)  |  行为的目标 |
| transition | int | 按钮切换的方式，目前包含 4 种[qc.Transition](../transition/README.md)，Transition.Node（不需要变换）、Transition.COLOR_TINT（变换颜色）、Transition.TEXTURE_SWAP（替换贴图）、Transition.ANIMATION（使用自定义动画） |
| disabledColor | [qc.Color](../color/README.md) | Transition.COLOR_TINT模式 && 置灰状态下的颜色 |
| disabledTexture | [asset.Atlas](../assets/Atlas.md) | Transition.TEXTURE_SWAP模式 && 置灰状态下的贴图 |
| normalColor | [qc.Color](../color/README.md) | Transition.COLOR_TINT模式 && 普通状态下的颜色 |
| normalTexture | [asset.Atlas](../assets/Atlas.md) | Transition.TEXTURE_SWAP模式 && 普通状态下的贴图 |
| pressedColor | [qc.Color](../color/README.md) | Transition.COLOR_TINT模式 && 按下状态下的颜色 |
| pressedTexture | [asset.Atlas](../assets/Atlas.md) | Transition.TEXTURE_SWAP模式 && 按下状态下的贴图 |

## 参考手册
[TransitionBehaviour](http://docs.zuoyouxi.com/manual/BuildinComponents/TransitionBehaviour.html)