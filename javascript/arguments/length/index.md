---
title: length
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/7474tyd4(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Returns the actual number of arguments passed to a function by the caller.'
tags:
  - JS
  - Basic
uri: javascript/arguments/length

---
## <span>Summary</span>

Returns the actual number of arguments passed to a function by the caller.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    [ function.] arguments.length

## <span>Examples</span>

The following example illustrates the use of the **length** property of the **arguments** object. To fully understand the example, pass more arguments to the function than the 2 arguments expected:

``` js
function ArgTest(a, b){
    var s = "";

    s += "Expected Arguments: " + ArgTest.length;
    s += "<br />";
    s += "Passed Arguments: " + arguments.length;

    document.write (s);
 }
```

## <span>Remarks</span>

The optional function argument is the name of the currently executing Function object.

The **length** property of the **arguments** object is initialized by the scripting engine to the actual number of arguments passed to a Function object when execution begins in that function.

## <span>See also</span>

### <span>Other articles</span>

-   [arguments Property (Function)](/javascript/Function/arguments)
-   [length Property (Array)](/javascript/Array/length)
-   [length Property (String)](/javascript/String/length)

