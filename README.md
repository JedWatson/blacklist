# blacklist

[![Version](http://img.shields.io/npm/v/blacklist.svg)](https://www.npmjs.org/package/blacklist)

This module shallow copies an object,  ignoring keys depending on the filter object passed to it.


### Example
``` javascript
var someInput = { a: 1, b: 2, c: 3 }

// ...

var blacklist = require('blacklist')

blacklist(someInput, {
	a: true,   // a will not be in the result
	b: false,  // b will be in the result
	c: 1 > 2   // false, therefore c will be in the result
})
// => { b: 2, c: 3 }
```
