---
title: concat
uri: 'concepts/programming/javascript/core objects/js/objects/String/concat'

---
### Summary

Returns value of joined strings without altering original string.

One of multiple ways to do this. Other ways include the addition operator ( + ) and the assignment operator ( += ).

### Syntax

``` js
"string".concat
```

### Parameters

string1, string2, stringN, etc...

### Example

``` js
var firstName="Patrick ";
var lastName="Wilson";
var describeThem=" is great";

var actorDescript = firstName.concat(lastName,describeThem);
```
