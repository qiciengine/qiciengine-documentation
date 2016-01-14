# Component Menu Customizing

By default, when click Add Component button, all scripts are displayed in Scripts submenu.
![Menu](images/1.png)  

If you want to change the display location of script, you can do it by setting __menu property of the script's behaviour class. 
Sample code:	
````javascript
var TestEditor = qc.defineBehaviour('qc.demo.TestEditor', qc.Behaviour, function() {
}, {
});

// setting __menu property for customizing the display location of qc.demo.TestEditor
TestEditor.__menu = 'Demo/Test';
````
