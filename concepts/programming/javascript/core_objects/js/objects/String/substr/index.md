---
title: substr
uri: 'concepts/programming/javascript/core objects/js/objects/String/substr'

---
### Summary

Returns a subset of a string starting at the given location through the given number of characters.

### Syntax

``` js
"string".substr(start [, length])
```

### Parameters

**start**

<dl>
<dd>
The location to start the subset of characters.

</dd>
</dl>
**length**

<dl>
<dd>
The number of characters to extract from the string.

</dd>
</dl>
### Example

``` js
var string = "The quick brown fox.";

print(string.substr(0, 3));     // "The"
print(string.substr(4));        // "quick brown fox."
print(string.substr(-3, 10));   // "ox."
```
