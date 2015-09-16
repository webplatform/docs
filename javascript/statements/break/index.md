---
title: break
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/3fhdxafb(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Terminates the current loop or, if in conjunction with a label, terminates the associated statement.'
tags:
  - JS
  - Basic
uri: javascript/statements/break

---
## Summary

Terminates the current loop or, if in conjunction with a label, terminates the associated statement.

## Syntax

<span class="language">JavaScript</span>

    break [ label ];

## Examples

In this example, the counter is set up to count from 1 to 99; however, the break statement terminates the loop after 14 counts.

``` js
for (var i = 1; i < 100; i++) {
     if (i == 15) {
         break;
     }
     document.write (i);
     document.write (" ");
 }

 // Output: 1234567891011121314
```

In the following code, the break statement refers to the for loop that is preceded by the `Inner:` statement. When `j` is equal to 24, the break statement causes the program flow to exit that loop. The numbers 21 through 23 print on each line.

``` js
Outer:
 for (var i = 1; i <= 10; i++) {
     document.write ("<br />");
     document.write ("i: " + i);
     document.write (" j: ");
 Inner:
     for (var j = 21; j <= 30; j++) {
         if (j == 24) {
             break Inner;
         }
         document.write (j + " ");
     }
 }

 // Output:
 // i: 1 j: 21 22 23
 // i: 2 j: 21 22 23
 // i: 3 j: 21 22 23
 // i: 4 j: 21 22 23
 // i: 5 j: 21 22 23
 // i: 6 j: 21 22 23
 // i: 7 j: 21 22 23
 // i: 8 j: 21 22 23
 // i: 9 j: 21 22 23
 // i: 10 j: 21 22 23
```

## Remarks

The optional label argument specifies the label of the statement you are breaking from.

You typically use the break statement in switch statements and in while , for , for...in , or do...while loops. You most commonly use the label argument in switch statements, but it can be used in any statement, whether simple or compound.

Executing the break statement exits from the current loop or statement, and begins script execution with the statement immediately following.

## See also

### Other articles

-   [continue Statement](/javascript/statements/continue)
-   [do...while Statement](/javascript/statements/do_while)
-   [for Statement](/javascript/statements/for)
-   [for...in Statement](/javascript/statements/for_in)
-   [Labeled Statement](/javascript/statements/Labeled)
-   [while Statement](/javascript/statements/while)

