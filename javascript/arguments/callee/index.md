---
title: 'callee'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/334e1zza(v=vs.94).aspx)'
compatibility:
  feature: callee
  topic: javascript
readiness: 'Ready to Use'
summary: 'Returns the Function object being executed, that is, the body text of the specified Function object.'
tags:
  - JS
  - Basic
uri: javascript/arguments/callee

---
## Summary

Returns the Function object being executed, that is, the body text of the specified Function object.

## Syntax

    [ function . ] arguments.callee

## Examples

``` js
function factorial(n){
   if (n <= 0)
      return 1;
   else
      return n * arguments.callee( n - 1 ) }
 document.write(factorial(4));
```

## Remarks

The optional function argument is the name of the currently executing Function object.

The **callee** property is a member of the **arguments** object that becomes available only when the associated function is executing.

The initial value of the **callee** property is the Function object being executed. This allows anonymous functions to be recursive.

## See also

### Other articles

-   [caller Property (Function)](/javascript/Function/caller)

