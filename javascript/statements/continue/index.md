---
title: 'continue'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/8de3fkc8(v=vs.94).aspx)'
compatibility:
  feature: continue
  topic: javascript
readiness: 'Ready to Use'
summary: 'Stops the current iteration of a loop, and starts a new iteration.'
tags:
  - JS_Basic
uri: javascript/statements/continue

---
## Summary

Stops the current iteration of a loop, and starts a new iteration.

## Syntax

    continue [ label ];

## Examples

In this example, a loop iterates from 1 through 9. The statements between continue and the end of the for body are skipped because of the use of the continue statement together with the expression `(i < 5)`.

``` js
for (var i = 1; i < 10; i++) {
     if (i < 5) {
         continue;
     }
     document.write (i);
     document.write (" ");
 }

 // Output: 5 6 7 8 9
```

In the following code, the continue statement refers to the for loop that is preceded by the `Inner:` label. When `j` is 24, the continue statement causes that for loop to go to the next iteration. The numbers 21 through 23 and 25 through 30 print on each line.

``` js
Outer:
 for (var i = 1; i <= 10; i++) {
     document.write ("<br />");
     document.write ("i: " + i);
     document.write (" j: ");

 Inner:
     for (var j = 21; j <= 30; j++) {
         if (j == 24) {
              continue Inner;
         }
         document.write (j + " ");
     }
 }

 //Output:
 //i: 1 j: 21 22 23 25 26 27 28 29 30
 //i: 2 j: 21 22 23 25 26 27 28 29 30
 //i: 3 j: 21 22 23 25 26 27 28 29 30
 //i: 4 j: 21 22 23 25 26 27 28 29 30
 //i: 5 j: 21 22 23 25 26 27 28 29 30
 //i: 6 j: 21 22 23 25 26 27 28 29 30
 //i: 7 j: 21 22 23 25 26 27 28 29 30
 //i: 8 j: 21 22 23 25 26 27 28 29 30
 //i: 9 j: 21 22 23 25 26 27 28 29 30
 //i: 10 j: 21 22 23 25 26 27 28 29 30
```

## Remarks

The optional label argument specifies the statement to which continue applies.

You can use the continue statement only inside a while , do...while , **for** , or for...in loop. Executing the continue statement stops the current iteration of the loop and continues program flow with the beginning of the loop. This has the following effects on the different types of loops:

-   while and do...while loops test their condition, and if true, execute the loop again.
-   for loops execute their increment expression, and if the test expression is true, execute the loop again.
-   for...in loops proceed to the next field of the specified variable and execute the loop again.

## See also

### Other articles

-   [break Statement](/javascript/statements/break)
-   [do...while Statement](/javascript/statements/do_while)
-   [for Statement](/javascript/statements/for)
-   [for...in Statement](/javascript/statements/for_in)
-   [Labeled Statement](/javascript/statements/Labeled)
-   [while Statement](/javascript/statements/while)

