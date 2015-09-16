---
title: 'arguments'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/he95z461(v=vs.94).aspx)'
compatibility:
  feature: arguments
  topic: javascript
readiness: 'Ready to Use'
summary: 'Gets the arguments for the currently executing Function object.'
tags:
  - JS
  - Basic
uri: javascript/Function/arguments

---
## Summary

Gets the arguments for the currently executing Function object.

## Syntax

    function.arguments

## Examples

The following example illustrates the use of the **arguments** property:

``` js
function ArgTest(arg1, arg2){
    var s = "";
    s += "The individual arguments are: "
    for (n = 0; n < arguments.length; n++){
       s += ArgTest.arguments[n];
       s += " ";
    }
    return(s);
 }
 document.write(ArgTest(1, 2, "hello"));

 //Output: function ArgTest(arg1, arg2){
    var s = "";
    s += "The individual arguments are: "
    for (n = 0; n < arguments.length; n++){
       s += ArgTest.arguments[n];
       s += " ";
    }
    return(s);
 }
 document.write(ArgTest(1, 2, "hello"));

 // Output: The individual arguments are: 1 2 hello
```

## Remarks

The function argument is the name of the currently executing function, and can be omitted.

This property allows a function to handle a variable number of arguments. The **length** property of the **arguments** object contains the number of arguments passed to the function. The individual arguments contained in the **arguments** object can be accessed in the same way array elements are accessed.

## See also

### Other articles

-   [arguments Object](/javascript/arguments)
-   [function Statement](/javascript/statements/function)

