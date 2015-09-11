---
title: toString
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/jj155283(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Returns a string representation of an error.'
tags:
  - JS
  - Basic
uri: javascript/Error/toString

---
## <span>Summary</span>

Returns a string representation of an error.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    error.toString()

**date**
:   Required. The error to represent as a string.

## <span>Return Value</span>

Returns "Error: " plus the error message.

## <span>Examples</span>

The following example illustrates the use of the **toString** method with an error.

``` js
var myError = new Error();
 myError.message = "My Error";
 var errorString = myError.toString();
 document.write(errorString);

 // Output: Error: My Error
```

