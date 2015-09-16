---
title: Labeled
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/d3666y5k(v=vs.94).aspx)'
notes:
  - 'Todo: Probably should be renamed to label.'
readiness: 'Ready to Use'
summary: 'Provides an identifier for a statement.'
tags:
  - JS
  - Basic
uri: javascript/statements/Labeled

---
## Summary

Provides an identifier for a statement.

## Syntax

<span class="language">JavaScript</span>

    label :
    statements

**label**
:   Required. A unique identifier used when referring to the labeled statement.

**statements**
:   Optional. One or more statements associated with label.

## Examples

In the following code, the **continue** statement refers to the **for** loop that is preceded by the `Inner:` statement. When `j` is 24, the **continue** statement causes that **for** loop to go to the next iteration. The numbers 21 through 23 and 25 through 30 print on each line.

``` js
Outer:
 for (i = 1; i <= 10; i++) {
    document.write ("<br />");
    document.write ("i: " + i);
    document.write (" j: ");

 Inner:
    for (j = 21; j <= 30; j++) {
       if (j == 24)
           {
           continue Inner;
       }
       document.write (j + " ");
   }
 }
```

## Remarks

Labels are used by the **break** and **continue** statements to specify the statement to which the **break** and **continue** apply.

## See also

### Other articles

-   [break Statement](/javascript/statements/break)
-   [continue Statement](/javascript/statements/continue)

