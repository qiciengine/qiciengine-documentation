# qc.TransitionBehaviour

## Description
A component for state change: normal、pressed、disable

## Variables
| Variable Name        |   Type       |  Description           |
| ------------- |-------------|-------------|
| target | [qc.Node](../gameobject/CNode.md)  |  The target node to apply transition. |
| transition | int | Transition mode: Transition.Node(No Transition), Transition.COLOR_TINT(Use an color tint transition), Transition.TEXTURE_SWAP(Use a sprite swap transition), Transition.ANIMATION(Use an animation transition) |
| disabledColor | [qc.Color](../color/README.md) | transition=Transition.COLOR_TINT && The color when disable |
| disabledTexture | [asset.Atlas](../assets/Atlas.md) | transition=Transition.TEXTURE_SWAP && The Texture when disable |
| normalColor | [qc.Color](../color/README.md) | transition=Transition.COLOR_TINT && The normal color |
| normalTexture | [asset.Atlas](../assets/Atlas.md) | transition=Transition.TEXTURE_SWAP && The normal texture |
| pressedColor | [qc.Color](../color/README.md) | transition=Transition.COLOR_TINT && The color when pressed |
| pressedTexture | [asset.Atlas](../assets/Atlas.md) | transition=Transition.TEXTURE_SWAP && The texture when pressed |

## Manual
[TransitionBehaviour](http://docs.qiciengine.com/manual/BuildinComponents/TransitionBehaviour.html)