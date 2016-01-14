# Local Storage
Most of the games need to save data to local or server, this chapter we'll introduce you the using of game.storage for local storage.

Notices:	
* If the browser's cache is cleared, then the data will lost
* Different game should set different game.bundleIdentifier value, or the data will conflict. See [Project Settings](../Settings/index.html)
* If you exceed the quota limit or in private browsing mode, then you should handle the exception throwed during the operations.

## Sample
````javascript
	// Set two items
	game.storage.set('name', 'QICI Engine');
	game.storage.set('mixed', {
		year: 2001,
		month: 10
	});

	// Save data to local
	game.storage.save();

	// Featch by key, get: 'QICI Engine'
	game.storage.get('name');

	// Delete one item by key
	game.storage.del('name');
````

## API
[game.storage](http://docs.qiciengine.com/api/storage/index.html)
