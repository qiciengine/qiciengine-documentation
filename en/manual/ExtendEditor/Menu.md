# Main Menu Extending

1. In Project panel, Create a script: Assets/Editor/ExtendEditor.js
````javascript
// Extend main menu
// The first parameter defines the path of the menu
// The second parameter definde the action with the menu is selected
G.extend.menu('Test/ClickMe', function() {
    alert('Welcome!');
});
````
2. Reload web page to check the result:		
	![Preview](images/menu.jpeg)  
	
## Demo
[Extend-menu Demo](http://engine.qiciengine.com/demo/misc/extend_editor/index.html)    