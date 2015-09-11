---
title: return
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/22a685h9(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Exits from the current function and returns a value from that function.'
tags:
  - JS
  - Basic
uri: javascript/statements/return

---
## <span>Summary</span>

Exits from the current function and returns a value from that function.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    return [ ( ][ expression ][ ) ];

## <span>Examples</span>

The following example illustrates the use of the return statement.

``` js
function myfunction(arg1, arg2){
    var r;
    r = arg1 * arg2;
    return(r);
 }
```

The following example illustrates the use of the return statement to return a function.

``` js
function doWork() {
     return function calculate(y) { return y + 1; };
 }

 var func = doWork();
 var x = func(5);
 document.write(x);

 // Output: 6
```

## <span>Remarks</span>

The optional expression argument is the value to be returned from the function. If omitted, the function does not return a value.

You use the return statement to stop execution of a function and return the value of expression. If expression is omitted, or no return statement is executed from within the function, the expression that called the current function is assigned the value undefined.

## <span>See also</span>

### <span>Other articles</span>

-   [function Statement](/javascript/statements/function)

