# Behaviour

The qc.defineBehaviour is used to be add to the node for extending UI logical behaviour. The behaviour works only when it's added on the node, can be displayed and modified data in Inspector panel.

## Define and Use Behaviour

The qc.defineBehaviour receives 4 params:  
1. The behaviour class name
2. The super class, use qc.Behaviour if not specified. Must be the subclass of qc.Behaviour
3. The class initalization function (When called, the behaviour doesn't be added to the node yet, and not finish deserialization yet.) 
4. Define the fields type that need to be serialized
````javascript
// Define a behaviour class: qc.demo.OnCollide    
var OnCollide = qc.defineBehaviour('qc.demo.OnCollide', qc.Behaviour, function() {
    this.clue = null;
}, 
{
	// define the property 'clue' to be serialized as Node type
    clue: qc.Serializer.NODE        
});
````

Add a behaviour to a node:  
````javascript
var script = node.addScript('qc.demo.OnCollide');
````

Get an added behaviour from a node:  
````javascript
var script = getScript('qc.demo.OnCollide');
````

Remove a behaviour from a node:  
````javascript
node.removeScript(script);
````

## Component-Oriented Programming
Component-oriented programming is different from object-oriented programming, it follows the composition over inheritance principle that allows greater flexibility in adding additional behavior or functionality on the node. The behaviour of a node can be changed at runtime by adding or removing component. This eliminates the ambiguity problems of deep and wide inheritance hierarchies that are difficult to understand, maintain and extend.

For exmaple, an UIImage node only has the ability to display image:  
1. If add a behaviour component with the onClick method implemented, then the image will has the interaction ability.
2. If add a animation behaviour, then the image will the animation function.
3. ...

## Built-in Behaviour methods
* __preUpdate, update, postUpdate__  
These methods will be called at every single frame automatically, if the behaviour is added on the node, and the node is visible, and the behaviour is enable.
* __awake__  
The awake method will be called when it's added to the node automatically.
* __onEnable, onDisable__  
When the behaviour's enable is changed from false to true, then the onEnable method is called, or the onDisable method is called.
* __onClick, onUp, onDown, onDrag, onDragStart, onDragEnd__  
These methods will be called during interaction, if the node's interactive is true.
* __onDestroy__  
When the behaviour is removed from the node, the onDestroy method will be called.


