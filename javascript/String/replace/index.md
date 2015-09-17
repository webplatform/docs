---
title: 'replace'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/t0kbytzc(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: "Replaces text in a string, using a regular expression or search string.\n"
tags:
  - JS_Basic
uri: javascript/String/replace

---
## Summary

Replaces text in a string, using a regular expression or search string.

## Syntax

    stringObj. replace( rgExp , replaceText )

**stringObj**
:   Required. The String object or string literal on which to perform the replacement. This string is not modified by the **replace** method. Rather, the return value of this method is the string produced by the replacement.

**rgExp**
:   Required. An instance of a **Regular Expression** object containing the regular expression pattern and applicable flags. Can also be a String object or string literal that represents the regular expression. If rgExp is not an instance of a **Regular Expression** object, it is converted to a string, and an exact search is made for the results; no attempt is made to convert the string into a regular expression.

**replaceText**
:   Required. A String object or string literal containing the text to replace for every successful match of rgExp in stringObj. In Internet Explorer 5.5 or later, the replaceText argument can also be a function that returns the replacement text.

## Return Value

The result of the **replace** method is a copy of stringObj after the specified replacements have been made.

## Remarks

Any of the following match variables can be used to identify the most recent match and the string from which it came. The match variables can be used in text replacement where the replacement string has to be determined dynamically.

|Characters|Meaning|
|:---------|:------|
|**\$\$**|\$ (Internet Explorer 5.5 or later)|
|**\$&**|Specifies that portion of stringObj that the entire pattern matched. (Internet Explorer 5.5 or later)|
|**\$\`**|Specifies that portion of stringObj that precedes the match described by **\$&**. (Internet Explorer 5.5 or later)|
|**\$'**|Specifies that portion of stringObj that follows the match described by **\$&**. (Internet Explorer 5.5 or later)|
|\$ n|The n th captured submatch, where n is a single decimal digit from 1 through 9. (Internet Explorer 5.5 or later)|
|\$ nn|The nn th captured submatch, where nn is a two-digit decimal number from 01 through 99. (Internet Explorer 5.5 or later)|

If replaceText is a function, for each matched substring the function is called with the following m + 3 arguments where m is the number of left capturing parentheses in the rgExp. The first argument is the substring that matched. The next m arguments are all of the captures that resulted from the search. Argument m + 2 is the offset within stringObj where the match occurred, and argument m + 3 is stringObj. The result is the string value that results from replacing each matched substring with the corresponding return value of the function call.

The **replace** method updates the properties of the global **RegExp** object.

## Examples

The following example illustrates the use of the **replace** method to replace all instances of "the" with "a."

``` js
var s = "the batter hit the ball with the bat";

 // Replace "the" with "a".
 var re = /the/g;
 var result = s.replace(re, "a");
 document.write(result);
 // Output: a batter hit a ball with a bat
```

In addition, the **replace** method can also replace subexpressions in the pattern. The following example exchanges each pair of words in the string.

``` js
var s = "The quick brown fox jumped over the lazy dog.";
 var re = /(\S+)(\s+)(\S+)/g;
 // Exchange each pair of words.
 var result = s.replace(re, "$3$2$1");
 document.write(result);

 // Output:  quick The fox brown over jumps lazy the dog.
```

The following example, which works in JavaScript 5.5 and later, shows how to use a function that returns the replacement text. It replaces any instance of a number followed by "F" with a Celsius conversion.

``` js
function f2c(s1) {
     // Initialize pattern.
     var test = /(\d+(\.\d*)?)F\b/g;

     // Use a function for the replacement.
     var s2 = s1.replace(test,
       function($0,$1,$2)
            {
            return((($1-32) * 5/9) + "C");
            }
         )
     return s2;
 }
 document.write(f2c("Water freezes at 32F and boils at 212F."));

 // Output: Water freezes at 0C and boils at 100C.
```

## See also

### Other articles

-   [exec Method (Regular Expression)](/javascript/regular_expression/exec)
-   [match Method (String)](/javascript/String/match)
-   [RegExp Object](/javascript/RegExp)
-   [search Method (String)](/javascript/String/search)
-   [test Method (Regular Expression)](/javascript/regular_expression/test)

