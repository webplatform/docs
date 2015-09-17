---
title: 'message'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/5z00ybxa(v=vs.94).aspx)'
compatibility:
  feature: message
  topic: javascript
readiness: 'Ready to Use'
summary: 'Returns an error message string.'
tags:
  - JS_Basic
uri: javascript/Error/message

---
## Summary

Returns an error message string.

## Syntax

    errorObj.message

**errorObj**
:   Required. Instance of Error object.

## Examples

The following example causes a TypeError exception to be thrown and displays the name of the error and its message.

``` js
try
 {
     // Cause an error.
     var x = y;
 }
 catch(e)
 {
     document.write ("Error Message: " + e.message);
     document.write ("<br />");
     document.write ("Error Code: ");
     document.write (e.number & 0xFFFF)
     document.write ("<br />");
     document.write ("Error Name: " + e.name);
 }
```

The output of this code is as follows.

``` js
Error Message: 'y' is undefined
 Error Code: 5009
 Error Name: TypeError
```

## Remarks

The message property returns a string that contains an error message associated with a specific error.

The description and message properties provide the same functionality. The description property provides backwards compatibility; the message property complies with the ECMA standard.

## See also

### Other articles

-   [description Property (Error)](/javascript/Error/description)
-   [name Property (Error)](/javascript/Error/name)

