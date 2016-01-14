# [qc.GS](README.md).registerCmd

## Prototype
* void registerCmd(cmd)

## Parameters
| Parameter | Type | Decription |
| ----------- | ----------- | ----------- |
| cmd | object | The command definition. See below. |

## Decription
Register a command processor. The processor defines:
````
	game.gs.registerCmd({
		// Command's name
		name: 'MSG_SAY',

		// The function of the command processor
		main: function(data) {
		}
	});
````
