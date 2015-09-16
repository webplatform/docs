---
title: Error
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/dww52sbt(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Contains information about errors.'
tags:
  - JS
  - Basic
uri: javascript/Error

---
## Summary

Contains information about errors.

## Syntax

<span class="language">JavaScript</span>

    errorObj = new Error()

<span class="language">JavaScript</span>

    errorObj = new Error([ number ])

<span class="language">JavaScript</span>

    errorObj = new Error([ number [, description ]])

**errorObj**
:   Required. The variable name to which the Error object is assigned.

**number**
:   Optional. Numeric value assigned to an error. Zero if omitted.

**description**
:   Optional. Brief string that describes an error. Empty string if omitted.

## Examples

The following example illustrates the use of the Error object.

``` js
function checkInput(x) {
     try
     {
         if (isNaN(parseInt(x))) {
             throw new Error("Input is not a number.");
         }
     }
     catch(e)
     {
         document.write(e.description);
     }
 }
```

The following example illustrates the use of the implicitly created Error object.

``` js
try
    {
    // Cause an error.
    x = y;
    }
 catch(e)
    {
       document.write(e);
       document.write ("<br />");

       document.write ("Number: ");
       document.write (e.number & 0xFFFF);
       document.write ("<br />");

       document.write ("Facility Code: ");
       document.write(e.number>>16 & 0x1FFF);
       document.write ("<br />");

       document.write ("Description: ");
       document.write (e.description);
    }

 // Output:
 // ReferenceError: 'y' is undefined
 // Facility Code: 10
 // Number: 5009
 // Description: 'y' is undefined
```

## Remarks

Whenever a run-time error occurs, an instance of the Error object is created to describe the error. This instance has two intrinsic properties that contain the description of the error ( **description** property) and the error number ( **number** property).

An error number is a 32-bit value. The upper 16-bit word is the facility code, while the lower word is the actual error code.

Error objects can also be explicitly created, using the syntax shown above, or thrown using the throw statement. In both cases, you can add any properties you choose to expand the capability of the Error object.

Typically, the local variable that is created in a **try...catch** statement refers to the implicitly created Error object. As a result, you can use the error number and description in any way you choose.

## Methods

[toString Method (Error)](/javascript/Error/toString) | [valueOf Method (Date)](/javascript/Date/valueOf)

## Properties

[constructor Property (Error)](/javascript/Error/constructor) | [number Property](/javascript/Error/description) | [prototype Property (Error)](/javascript/Error/prototype) | [stack Property (Error)](/javascript/Error/stack) | [stackTraceLimit Property (Error)](/javascript/Error/stackTraceLimit)

## See also

### Other articles

-   [new Operator](/javascript/operators/new)
-   [throw Statement](/javascript/statements/throw)
-   [try...catch...finally Statement](/javascript/statements/try_catch_finally)
-   [var Statement](/javascript/statements/var)

