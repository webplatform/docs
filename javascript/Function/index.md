---
title: Function
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/x844tc74(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Creates a new function.'
tags:
  - JS
  - Basic
uri: javascript/Function

---
## Summary

Creates a new function.

## Syntax

<span class="language">JavaScript</span>

    function functionName ( [ argname1  [, ...[, argnameN ] ] ] )

<span class="language">JavaScript</span>

    functionName = new Function( [ argname1 ,  [... argnameN ,] ] body );

**functionName**
:   Required. The name of the newly created function

**argname1...argnameN**
:   Optional. A list of arguments the function accepts.

**parameters**
:   Optional. Parameters are the named arguments in the function declaration's arguments list. Parameters must be valid identifiers. If there is more than one, parameters are separated by commas.

**body**
:   Optional. A string that contains the block of JavaScript code to be executed when the function is called.

## Examples

To declare a function that adds the two arguments passed to it, you can do it in one of two ways:

``` js
//Method 1
 function add(x, y)
 {
    return(x + y);
 }

//Method 2
 var add = function(x, y) {
      return(x+y);
 }

//In either case, you call the function with a line of code similar to this:
 add(2, 3);
```

## Remarks

The function is a basic data type in JavaScript. Syntax 1 creates a function value that JavaScript converts into a Function object when necessary. JavaScript converts Function objects created by Syntax 2 into function values at the time the function is called.

Syntax 1 is the standard way to create new functions in JavaScript. Syntax 2 is an alternative form used to create function objects explicitly.

**Note** -- When you call a function, make sure that you always include the parentheses and any required arguments. Calling a function without parentheses causes the function itself to be returned, instead of the return value of the function.

## Properties

[prototype Property](/javascript/arguments/0_n_Properties)

## Methods

[valueOf Method](/javascript/Function/apply)

## See also

### Other articles

-   [function Statement](/javascript/statements/function)
-   [new Operator](/javascript/operators/new)
-   [var Statement](/javascript/statements/var)

