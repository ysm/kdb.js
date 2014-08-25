kdb.js
======

JavaScript wrapper for kdb+ websockets. Makes it easier to develop web applications for kdb.

Usage:
```
var kdb = new KDB("localhost", 5002);
kdb.query("239*239", function(data) {
  console.log(data);
});
```
