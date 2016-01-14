# qc.Debug

## Description
The module for debug. This class represents a singleton object that can be accessed directly as `game.debug`.  
By default, Debug is enable in editor and disable when published.

## Variables
| Variable Name | Type | Description |
| ------------- |-------------|-------------|
| game | [qc.Game](../Game/README.md) | The local game reference. |
| on | boolean | Is the debug enable? If true, [Log](../log/README.md) enableTrace is true too. |
