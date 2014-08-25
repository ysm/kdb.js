kdb.js
======

JavaScript wrapper for kdb+ websockets. Makes it easier to develop web applications for kdb.

Usage:
```
var kdb = new KDB("localhost", 1234);
kdb.query("239*239", function(data) {
  console.log(data);
});
```

This will work after loading necessary JS files:
* kdb.js itself
* [c.js](http://kx.com/q/c/c.js) from kx wiki
 
In your q script you will need to:

1. Load [json.k](http://kx.com/q/e/json.k) from kx wiki
2. Define .z.ws function 
3. Open port to start accepting connections
```
\l json.k
.z.ws:{neg[.z.w] -8! value -9!x};
\p 1234
```

See examples in sample.html and script.q.
