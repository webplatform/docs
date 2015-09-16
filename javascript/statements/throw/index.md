---
title: throw
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/85fscz6h(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Generates an error condition that can be handled by a try...catch...finally statement.'
tags:
  - JS
  - Basic
uri: javascript/statements/throw

---
## Summary

Generates an error condition that can be handled by a try...catch...finally statement.

## Syntax

<span class="language">JavaScript</span>

    throw exception

## Examples

The following example throws an error inside a try block, and it is caught in the catch block.

``` js
try {
         throw new Error(200, "x equals zero");
 }
 catch (e) {
     document.write(e.message);
 }

 // Output: x equals zero.
```

## Remarks

The required exception argument can be any expression.

## See also

### Other articles

-   [try...catch...finally Statement](/javascript/statements/try_catch_finally)
-   [Error Object](/javascript/Error)

