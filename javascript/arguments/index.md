---
title: 'arguments'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/87dw3w1k(v=vs.94).aspx)'
compatibility:
  feature: arguments
  topic: javascript
readiness: 'Ready to Use'
summary: 'An object representing the arguments to the currently executing function, and the functions that called it.'
tags:
  - JS
  - Basic
uri: javascript/arguments

---
## Summary

An object representing the arguments to the currently executing function, and the functions that called it.

## Syntax

    [ function . ] arguments[ n ]

**function**
:   Optional. The name of the currently executing Function object.

**n**
:   Required. The zero-based index to argument values passed to the Function object.

## Examples

The following example illustrates the use of the **arguments** object.

``` js
function ArgTest(a, b)
 {
    var s = "";

    s += "Expected Arguments: " + ArgTest.length;
    s += "<br />";
    s += "Passed Arguments: " + arguments.length;
    s += "<br />";

    s += "The individual arguments are: "
    for (n = 0; n < arguments.length; n++)
    {
       s += ArgTest.arguments[n];
       s += " ";
    }

    document.write(s);
 }

 ArgTest(1, 2, "hello", new Date())

 // Output:
 // Expected Arguments: 2
 // Passed Arguments: 4
 // The individual arguments are: 1 2 hello Tues Jan 8 08:27:09 PST 20xx
```

## Remarks

You cannot explicitly create an **arguments** object. The **arguments** object only becomes available when a function begins execution. The **arguments** object of the function is not an array, but the individual arguments are accessed the same way array elements are accessed. The index n is actually a reference to one of the **0** n properties of the **arguments** object.

## See also

### Other articles

-   [0...n Properties (arguments)](/javascript/arguments/0_n_Properties)
-   [callee Property (arguments)](/javascript/arguments/callee)
-   [length Property (arguments)](/javascript/arguments/length)

