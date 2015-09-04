---
title: length
tags:
  - JS
  - Basic
readiness: 'Ready to Use'
summary: 'Returns the actual number of arguments passed to a function by the caller.'
uri: javascript/arguments/length

---
# length

## Summary

Returns the actual number of arguments passed to a function by the caller.

## Syntax

    [ function.] arguments.length

## Examples

The following example illustrates the use of the **length** property of the **arguments** object. To fully understand the example, pass more arguments to the function than the 2 arguments expected:

``` {.js}
function ArgTest(a, b){
    var s = "";

    s += "Expected Arguments: " + ArgTest.length;
    s += "<br />";
    s += "Passed Arguments: " + arguments.length;

    document.write (s);
 }
```

## Remarks

The optional function argument is the name of the currently executing Function object.

The **length** property of the **arguments** object is initialized by the scripting engine to the actual number of arguments passed to a Function object when execution begins in that function.

## See also

### Other articles

-   [arguments Property (Function)](/javascript/Function/arguments)
-   [length Property (Array)](/javascript/Array/length)
-   [length Property (String)](/javascript/String/length)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/7474tyd4(v=vs.94).aspx)

