---
title: 0...n Properties
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/bb79e676(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Returns the actual value of individual arguments from an arguments object returned by the arguments property of an executing function.'
tags:
  - JS
  - Basic
uri: 'javascript/arguments/0 n Properties'

---
## <span>Summary</span>

Returns the actual value of individual arguments from an arguments object returned by the arguments property of an executing function.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    [ function . ] arguments[ [0|1|2|...| n ] ]

**function**
:   Optional. The name of the currently executing Function object.

**0, 1, 2, , n**
:   Required. Non-negative integer in the range of 0 to n where 0 represents the first argument and n represents the final argument. The value of the final argument n is **arguments.length-1**.

## <span>Examples</span>

The following example illustrates the use of the **0 . . .** n properties of the **arguments** object. To fully understand the example, pass one or more arguments to the function:

``` js
function ArgTest(){
    var s = "";
    s += "The individual arguments are: "
    for (n = 0; n < arguments.length; n++){
       s += ArgTest.arguments[n] ;
       s += " ";
    }
    return(s);
 }
 document.write(ArgTest(1, 2, "hello", new Date()));
```

## <span>Remarks</span>

The values returned by the 0 . . . n properties are the actual values passed to the executing function. While not actually an array of arguments, the individual arguments that comprise the **arguments** object are accessed the same way that array elements are accessed.

## <span>See also</span>

### <span>Other articles</span>

-   [length Property (arguments)](/javascript/arguments/length)
-   [length Property (Function)](/javascript/Function/length)

