---
title: valueOf
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/jj155293(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Returns the string value of an error.'
tags:
  - JS
  - Basic
uri: javascript/Error/valueOf

---
## <span>Summary</span>

Returns the string value of an error.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    error.valueOf()

## <span>Return Value</span>

The string "Error: " plus the error message.

## <span>Examples</span>

The following example illustrates the use of the **valueOF** method with a date.

``` js
var myError = new Error();
 myError.message = "This is an error.";
 var value = myError.valueOf();
 document.write(value);

 // Output: Error: This is an error.
```

## <span>Remarks</span>

The error object is any instance of an Error.

