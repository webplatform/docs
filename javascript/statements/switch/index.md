---
title: switch
tags:
  - JS
  - Basic
readiness: 'Ready to Use'
summary: 'Enables the execution of one or more statements when a specified expression''s value matches a label.'
uri: javascript/statements/switch

---
# switch

## Summary

Enables the execution of one or more statements when a specified expression's value matches a label.

## Syntax

    switch ( expression ) {
         case label:
             statementlist
         case label:
         default:
             statementlist
    }

**expression**
:   The expression to be evaluated.

**label**
:   An identifier to be matched against expression. If label is an expression , execution starts with the statementlist immediately after the colon, and continues until it encounters either a break statement, which is optional, or the end of the switch statement.

**statementlist**
:   One or more statements to be executed.

## Examples

The following example tests an object for its type.

``` {.js}
function MyObjectType(obj) {
     switch (obj.constructor) {
         case Date:
             document.write("Object is a Date.");
             break;
         case Number:
             document.write("Object is a Number.");
             break;
         case String:
             document.write("Object is a String.");
             break;
         default:
             document.write("Object is unknown.");
     }
 }

 // Output when obj is a Date:
 // Object is a Date.

 // Output when obj is a Number:
 // Object is a Number.

 // Output when obj is a String:
 // Object is a String.

 // Output when obj is something other than a Date, Number, or String:
 // Object is unknown.
```

The following code shows what happens if you do not use a break statement.

``` {.js}
function MyObjectType(obj) {
     switch (obj.constructor) {
         case Date:
             document.write("Object is a Date.");
         case Number:
             document.write("Object is a Number.");
         case String:
             document.write("Object is a String.");
         default:
             document.write("Object is unknown.");
     }
 }

 // Output when obj is a Date:
 // Object is a Date.Object is a Number.Object is a String.Object is unknown.

 // Output when obj is a Number:
 // Object is a Number.Object is a String.Object is unknown.

 // Output when obj is a String:
 // Object is a String.Object is unknown.

 // Output when obj is something other than a Date, Number, or String:
 // Object is unknown.
```

## Remarks

Use the default clause to provide a statement to be executed if none of the label values matches expression. It can appear anywhere within the switch code block.

Zero or more label blocks may be specified. If no label matches the value of expression , and a default case is not supplied, no statements are executed.

Execution flows through a switch statement as follows:

-   Evaluate expression and look at label in order until a match is found.
-   If a label value equals expression , execute its accompanying statementlist.Continue execution until a break statement is encountered, or the switch statement ends. This means that multiple label blocks are executed if a break statement is not used.
-   If no label equals expression , go to the default case. If there is no default case, go to last step.
-   Continue execution at the statement following the end of the switch code block.

## See also

### Other articles

-   [break Statement](/javascript/statements/break)
-   [if...else Statement](/javascript/statements/if_else)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/hzc6t81t(v=vs.94).aspx)

