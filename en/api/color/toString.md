# qc.Color#toString

## Prototype
* void toString(patten:string);

## Description
Convert a Color to string.

## Sample
````
	var c = new qc.Color('#ffffff');

	// output: RGBA(255,255,255,1)
	c.toString('rgba');

	// output: RGB(255,255,255)
	c.toString('rgb');

	// output: #FFFFFF
	c.toString('#rgb');

	// output: #FFFFFFFF
	c.toString('#argb');
````
