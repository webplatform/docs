---
title: eval
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/12k71sw7(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Evaluates JavaScript code and executes it.'
tags:
  - JS
  - Basic
uri: javascript/eval

---
## Summary

Evaluates JavaScript code and executes it.

## Syntax

    eval( codeString )

**codeString**
:   Required. A **String** value that contains valid JavaScript code.

## Examples

The following code initializes the variable `myDate` to a test date.

``` js
var dateFn = "Date(1971,3,8)";
 var myDate;
 eval("myDate = new " + dateFn + ";");

 document.write(myDate);

 // Output: Thu Apr 8 00:00:00 PDT 1971
```

## Remarks

The **eval** function enables dynamic execution of JavaScript source code.

The codeString string is parsed by the JavaScript parser and executed.

The code passed to the **eval** function is executed in the same context as the call to the **eval** function.

Whenever possible, use the [JSON.parse function](/javascript/JSON/parse) to de-serialize JavaScript Object Notation (JSON) text. The **JSON.parse** function is more secure and executes faster than the **eval** function.

## See also

### Other articles

-   [String Object](/javascript/String)

