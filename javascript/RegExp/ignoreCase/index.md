---
title: ignoreCase
tags:
  0: JS
  1: Basic
  3: Property
readiness: 'Ready to Use'
notes:
  - 'Moved under javascript/RegExp'
summary: 'Returns a Boolean value indicating the state of the ignoreCase flag ( i ) used with a regular expression. Default is false. Read-only.'
uri: javascript/RegExp/ignoreCase

---
# ignoreCase

## Summary

Returns a Boolean value indicating the state of the ignoreCase flag ( i ) used with a regular expression. Default is false. Read-only.

## Syntax

    rgExp.ignoreCase

## Examples

The following example illustrates the use of the **ignoreCase** property. If you pass "gi" in to the function shown below, all instances of the word "the" are replaced with the word "a", including the initial "The". This is because with the ignoreCase flag set, the search ignores any case sensitivity. So "T" is the same as "t" for the purposes of matching.

This function returns the Boolean values that indicate the state of the allowable regular expression flags, which are **g** , **i** , and **m**. The function also returns the string with all replacements made.

``` {.js}
function RegExpPropDemo(flag){
     // The flag parameter is a string that contains
     // g, i, or m. The flags can be combined.

     // Check flags for validity.
     if (flag.match(/[^gim]/))
         {
         return ("Flag specified is not valid");
         }

     // Create the string on which to perform the replacement.
     var orig = "The batter hit the ball with the bat ";
     orig += "and the fielder caught the ball with the glove.";

     // Replace "the" with "a".
     var re = new RegExp("the", flag);
     var r = orig.replace(re, "a");

     // Output the resulting string and the values of the flags.
     var s = "";
     s += "global: " + re.global.toString();
     s += "<br />";
     s += "ignoreCase: " + re.ignoreCase.toString();
     s += "<br />";
     s += "multiline: " + re.multiline.toString();
     s += "<br />";
     s += "Resulting String: " + r;
     s += "<br />";
     s += "<br />";
     return (s);
 }

 document.write(RegExpPropDemo("gi"));
 document.write(RegExpPropDemo("g"));
```

Following is the resulting output.

``` {.js}
global: true
 ignoreCase: true
 multiline: false
 Resulting String: a batter hit a ball with a bat and a fielder caught a ball with a glove.

 global: true
 ignoreCase: false
 multiline: false
 Resulting String: The batter hit a ball with a bat and a fielder caught a ball with a glove.
```

## Remarks

The required rgExp reference is an instance of the **RegExp** object.

The **ignoreCase** property returns **true** if the ignoreCase flag is set for a regular expression, and returns **false** if it is not.

The ignoreCase flag, when used, indicates that a search should ignore case sensitivity when matching the pattern within the searched string.

## See also

### Other articles

-   [global Property (Regular Expression)](/javascript/regular_expression/global)
-   [multiline Property (Regular Expression)](/javascript/regular_expression/multiline)
-   [sticky Property (Regular Expression)](/javascript/regular_expression/sticky)
-   [unicode Property (Regular Expression)](/javascript/regular_expression/unicode)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/8kz93es5(v=vs.94).aspx)

