---
title: description
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/hs13sc3e(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Returns or sets the descriptive string associated with a specific error.'
tags:
  - JS
  - Basic
uri: javascript/Error/description

---
## <span>Summary</span>

Returns or sets the descriptive string associated with a specific error.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    object .description  [ =  stringExpression ]

**object**
:   Required. Any instance of an Error object.

**stringExpression**
:   Optional. A string expression containing a description of the error.

## <span>Examples</span>

The following example illustrates the use of the **description** property.

``` js
try
 {
 // Cause an error:
     x = y
 }
 catch(e)
 {
 // Prints "[object Error]":
     document.write(e)
     document.write (" ");
 // Prints 5009:
     document.write((e.number & 0xFFFF))
     document.write (" ");
 // Prints "'y' is undefined":
     document.write(e.description);
     document.write (" ");
 // Prints "'y' is undefined":
     document.write(e.message)
 }
```

## <span>Remarks</span>

The **description** property contains the error message string associated with a specific error. Use the value contained in this property to alert a user to an error.

The **description** and **message** properties provide the same functionality; the **description** property provides backward compatibility; the **message** property complies with the ECMA standard.

## <span>See also</span>

### <span>Other articles</span>

-   [number Property (Error)](/javascript/Error/number)
-   [message Property (Error)](/javascript/Error/message)
-   [name Property (Error)](/javascript/Error/name)

