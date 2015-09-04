---
title: stack
tags:
  - JS
  - Basic
readiness: 'Ready to Use'
summary: 'Gets or sets the error stack as a string that contains the stack trace frames.'
uri: javascript/Error/stack

---
# stack

## Summary

Gets or sets the error stack as a string that contains the stack trace frames.

## Syntax

    object .stack

## Examples

The following example shows how to get the stack when you're catching an error.

``` {.js}
try
     {
         var x = y.name;
     }
 catch(e)
     {
         document.write ("Error stack: ")
         document.write (e.stack);
     }
```

The following example shows how to set and then get the stack.

``` {.js}
try
     {
         var err = Error("my error");
         err.stack = "my stack trace";
         throw err;
     }
 catch(e)
     {
         document.write ("Error stack: ")
         document.write (e.stack);
     }
```

## Remarks

The **stack** property is set to undefined when the error is constructed, and gets the trace information when the error is raised. If an error is raised multiple times, the **stack** property is updated each time the error is raised.

Stack frames are displayed in the following format: at FunctionName (\<Fully-qualified name/URL\>:\<line number\>:\<column number\>)

If you create your own Error object and set the stack trace to a value, the value won't be overwritten when the error is thrown.

The **stack** property does not show inline functions in its frames. It shows only the physical stack.

## See also

### Other articles

-   [description Property (Error)](/javascript/Error/description)
-   [message Property (Error)](/javascript/Error/message)
-   [name Property (Error)](/javascript/Error/name)
-   [stackTraceLimit Property (Error)](/javascript/Error/stackTraceLimit)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/hh699850(v=vs.94).aspx)

