---
title: 'number'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/hc53e755(v=vs.94).aspx)'
compatibility:
  feature: number
  topic: javascript
readiness: 'Ready to Use'
summary: 'Returns or sets the numeric value associated with a specific error. The Error object''s default property is number.'
tags:
  - JS_Basic
uri: javascript/Error/number

---
## Summary

Returns or sets the numeric value associated with a specific error. The Error object's default property is number.

## Syntax

    object .number [ =  errorNumber ]

**Object**
:   Any instance of the Error object.

**errorNumber**
:   An integer representing an error.

## Examples

The following example causes an exception to be thrown and displays the error code that is derived from the error number.

``` js
try
     {
     // Cause an error.
     var x = y;
     }
 catch(e)
     {
     document.write ("Error Code: ");
     document.write (e.number & 0xFFFF)
     document.write ("<br />");

     document.write ("Facility Code: ")
     document.write(e.number>>16 & 0x1FFF)
     document.write ("<br />");

     document.write ("Error Message: ")
     document.write (e.message)
     }
```

The output of this code is as follows.

``` js
Error Code: 5009
 Facility Code: 10
 Error Message: 'y' is undefined
```

## Remarks

An error number is a 32-bit value. The upper 16-bit word is the facility code, and the lower word is the error code. To determine the error code, use the & (bitwise And) operator to combine the number property with the hexadecimal number `0xFFFF`.

## See also

### Other articles

-   [description Property (Error)](/javascript/Error/description)
-   [message Property (Error)](/javascript/Error/message)
-   [name Property (Error)](/javascript/Error/name)

