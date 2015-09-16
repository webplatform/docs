---
title: function
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/4t2k5yhw(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Declares a new function.'
tags:
  0: JS
  1: Basic
  3: Function
uri: javascript/statements/function

---
## Summary

Declares a new function.

## Syntax

<span class="language">JavaScript</span>

    function functionName ([ arg1 [, arg2 [,...[, argN ]]]] ) {
         statements
    }

**functionName**
:   Required. The name of the function.

**arg1...argN**
:   Optional. An optional, comma-separated list of arguments the function understands.

**statements**
:   Optional. One or moreJavaScript statements.

## Examples

The following example illustrates the use of the function statement.

``` js
//Defining the function myFunc
function myFunc () {
    var r = 3 * 4;
    return(r);
}

//Calling the function
myFunc();

//Output: 12
```

It's possible to pass along arguments within the parantheses when calling the function.

``` js
//Defining the function myFunc
function myFunc (name) {
    console.log('Hello, ' + name + '!');
}

//Calling the function
myFunc('Susan');

//Output: Hello, Susan!
```

A function can be assigned to a variable. This is illustrated in the following example.

``` js
function addFive(x) {
     return x + 5;
 }

 function addTen(x) {
     return x + 10;
 }

 var condition = false;

 var myFunc;
 if (condition) {
     myFunc = addFive;
 }
 else {
     myFunc = addTen;
 }

 var result = myFunc(123);
 // Output: 133
```

## Remarks

Use the function statement to declare a function for later use. The code that is contained in statements is not executed until the function is called from elsewhere in the script.

The [return](/javascript/statements/return) statement is used to return a value from the function. You do not have to use a return statement; the program will return when it reaches the end of the function. If no return statement is executed in the function, or if the return statement has no expression, the function returns the value undefined.

**Note** -- When you call a function, be sure to include the parentheses and any required arguments. Calling a function without parentheses returns a reference to the function, not the results of the function.

## See also

### Other articles

-   [new Operator](/javascript/operators/new)

