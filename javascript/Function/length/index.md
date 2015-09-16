---
title: length
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/4cz6db7d(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Gets the number of arguments defined for a function.'
tags:
  - JS
  - Basic
uri: javascript/Function/length

---
## Summary

Gets the number of arguments defined for a function.

## Syntax

<span class="language">JavaScript</span>

    functionName.length

## Examples

The following example illustrates the use of the **length** property:

``` js
function ArgTest(a, b){
     var s = "";

     s += "Expected Arguments: " + ArgTest.length;
     s += "<br />";
     s += "Passed Arguments: " + arguments.length;

     return s;
 }

 document.write(ArgTest(1, 2));

 // Output:
 // Expected Arguments: 2
 // Passed Arguments: 2
```

## Remarks

The required functionName is the name of the function.

The **length** property of a function is initialized by the scripting engine to the number of arguments in the function's definition when an instance of the function is created.

What happens when a function is called with a number of arguments different from the value of its **length** property depends on the function.

## See also

### Other articles

-   [arguments Property (Function)](/javascript/Function/arguments)
-   [length Property (Array)](/javascript/Array/length)
-   [length Property (String)](/javascript/String/length)

