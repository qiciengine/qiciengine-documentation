# qc.Behaviour

## Description
Base class for everything attached to GameObjects.

Note that your code will never directly create a Behaviour. Instead, you write script code, and attach the script to a GameObject(Node).

## Define a Behaviour
````
	// Prototype
	qc.defineBehaviour = function(clazz:string, parent:class, init:function, fields:object);

	// Sample: Define "qc.demo.Test"
	qc.defineBehaviour('qc.demo.Test', qc.Behaviour, function() {
		// Init here
		this.year = 2015;
	}, {
		// Serializable fields
		year: qc.Serializer.NUMBER
	})
````

## Variables
| Variable Name        | Description           |
| ------------- |-------------|
| gameObject:[qc.Node](../gameobject/node.md) | The Node for attatching this behaviour. |
| name:string | The name of the node. |
| enable: boolean| Enabled Behaviours are Updated, disabled Behaviours are not. |
| runInEditor: boolean| Default false. If true the bahaviours are updated in editor. |
| game: [qc.Game](../game/README.md) | Read only. Local reference to game. |

## Methods
| Method | Description |
| ------------- |-------------|
| getScript | See: [Node.getScript](../gameobject/node_getScript.md) |
| getScripts | See: [Node.getScripts](../gameobject/node_getScripts.md) |
| [destroy](destroy.md) | Destroy the behaviour. When destroyed, the function 'onDestroy' will be called. |
| [addListener](addListener.md) | Listen event hook, it will be removed automatically when object destroy. |

## Callback
| Method | Description |
| ------------- |-------------|
| awake | Awake is called when the script instance is being loaded. |
| preUpdate | This function is called every fixed framerate frame, if the Behaviour is enabled. |
| update | Update is called every frame, if the Behaviour is enabled. |
| postUpdate | postUpdate is called every frame, if the Behaviour is enabled. |
| render | render is called every frame, if the Behaviour is enabled. |
| postRender | postRender is called every frame, if the Behaviour is enabled. |
| onDown | When the  pointer pressed, onDown is called. |
| onUp | When the pointer released, onUp is called. |
| onClick | When clicked, onClick is called. |
| onDragStart | When starting a drag operation, onDragStart is called.  |
| onDrag | When dragging, onDrag is called. |
| onDragEnd | When ending a drag operation, onDragEnd is called. |
| isAllowDrop | Whether the node can drop here? |
| onEnable | This function is called when the object becomes enabled and active. |
| onDisable | This function is called when the behaviour becomes disabled or inactive. |
| onDestroy | This function is called when the behaviour will be destroyed. |

## Sample
