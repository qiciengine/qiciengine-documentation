# qc.GS

## Decription
The connector to the game server.  
This class represents a singleton object that can be accessed directly as `game.gs`.  

## Varaibles
| Varaible    | Type    | Decription           |
| ------------- |-------------|-------------|
| game | [qc.Game](../game/README.md) | Read only. The local game reference. |
| autoReconnect | boolean | When disconnect, auto reconnect? Default:false. |
| isConnected | boolean | Read only. Is the client connected to the game server? |

## Events
| Event | Decription |
| ------------- |-------------|
| onConnected | When connected to the game server, this event is triggered. |
| onDisconnect | When disconnect from the game server, this event is triggered. |

## Methods
| Method | Decription |
| ------------- |-------------|
| [connect](connect.md) | Connect to the game server. |
| [disconnect](disconnect.md) | Disconnect from the game server. |
| [sendMessage](sendMessage.md) | Send a command to the game server. |
| [registerCmd](registerCmd.md) | Register a command processor. |
