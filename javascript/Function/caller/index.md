---
title: caller
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/7t96kt3h(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Gets the function that invoked the current function.'
tags:
  - JS
  - Basic
uri: javascript/Function/caller

---
## Summary

Gets the function that invoked the current function.

## Syntax

<span class="language">JavaScript</span>

    functionName.caller

## Examples

The following example illustrates the use of the **caller** property:

``` js
function CallLevel(){
    if ( CallLevel.caller == null)
       return("CallLevel was called from the top level.");
    else
       return("CallLevel was called by another function.");
 }

 document.write(CallLevel());

 // Output: CallLevel was called from the top level.
```

## Remarks

The functionName object is the name of any executing function.

The **caller** property is defined for a function only while that function is executing. If the function is called from the top level of a JavaScript program, **caller** contains null.

If the **caller** property is used in a string context, the result is the same as functionName.**toString** , that is, the decompiled text of the function is displayed.

## See also

### Other articles

-   [function Statement](/javascript/statements/function)

