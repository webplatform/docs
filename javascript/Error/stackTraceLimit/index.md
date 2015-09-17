---
title: 'stackTraceLimit'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/hh699849(v=vs.94).aspx)'
compatibility:
  feature: stackTraceLimit
  topic: javascript
readiness: 'Ready to Use'
summary: 'Gets or sets the stack trace limit, which is equivalent to the number of error frames to display. The default limit is 10.'
tags:
  - JS_Basic
uri: javascript/Error/stackTraceLimit

---
## Summary

Gets or sets the stack trace limit, which is equivalent to the number of error frames to display. The default limit is 10.

## Syntax

    Error .stackTraceLimit

## Examples

The following example shows how to set and then get the stack trace limit.

``` js
try
     {
     var err = new Error("my error");
     Error.stackTraceLimit = 7;
     throw err;
     }
 catch(e)
     {
     document.write ("Error stack trace limit: ")
     document.write (Error.stackTraceLimit);
     }
```

## Remarks

You can set the **stackTraceLimit** property to any positive value between 0 and Infinity. If the **stackTraceLimit** property is set to 0 at the time an error is thrown, no stack trace is shown. If the property is set to a negative value or a non-numeric value, the value is converted to 0. If the stackTraceLimit is set to Infinity , the entire stack is shown. Otherwise, ToUint32 is used to convert the value.

## See also

### Other articles

-   [description Property (Error)](/javascript/Error/description)
-   [message Property (Error)](/javascript/Error/message)
-   [name Property (Error)](/javascript/Error/name)
-   [stack Property (Error)](/javascript/Error/stack)

