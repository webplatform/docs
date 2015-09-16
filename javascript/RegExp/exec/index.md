---
title: exec
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/z908hy33(v=vs.94).aspx)'
notes:
  - 'Moved under javascript/RegExp'
readiness: 'Ready to Use'
summary: 'Executes a search on a string using a regular expression pattern, and returns an array containing the results of that search.'
tags:
  0: JS
  1: Basic
  3: Method
uri: javascript/RegExp/exec

---
## Summary

Executes a search on a string using a regular expression pattern, and returns an array containing the results of that search.

## Syntax

    rgExp.exec( str )

**rgExp**
:   Required. An instance of a **Regular Expression** object containing the regular expression pattern and applicable flags.

**str**
:   Required. The String object or string literal on which to perform the search.

## Examples

The following example illustrates the use of the **exec** method:

``` js
function RegExpTest()
 {
    var ver = Number(ScriptEngineMajorVersion() + "." + ScriptEngineMinorVersion())
    if (ver < 5.5)
    {
       document.write("You need a newer version of JavaScript for this to work");
       return;
    }

    var src = "The quick brown fox jumps over the lazy dog.";

    // Create regular expression pattern with a global flag.
    var re = /\w+/g;

    // Get the next word, starting at the position of lastindex.
    var arr;
    while ((arr = re.exec(src)) != null)
       {
       // New line:
       document.write ("<br />");
       document.write (arr.index + "-" + arr.lastIndex + " ");
       document.write (arr[0]);
       }
 }
```

## Remarks

If the **exec** method does not find a match, it returns null. If it finds a match, **exec** returns an array, and the properties of the global **RegExp** object are updated to reflect the results of the match. Element zero of the array contains the entire match, while elements 1 - n contain any submatches that have occurred within the match. This behavior is identical to the behavior of the **match** method without the global flag ( **g** ) set.

If the global flag is set for a regular expression, **exec** searches the string beginning at the position indicated by the value of **lastIndex**. If the global flag is not set, **exec** ignores the value of **lastIndex** and searches from the beginning of the string.

The array returned by the **exec** method has three properties, **input** , **index** and **lastIndex.** The **input** property contains the entire searched string. The **index** property contains the position of the matched substring within the complete searched string. The **lastIndex** property contains the position following the last character in the match.

## See also

### Other articles

-   [match Method (String)](/javascript/String/match)
-   [RegExp Object](/javascript/RegExp)
-   [search Method (String)](/javascript/String/search)
-   [test Method (Regular Expression)](/javascript/regular_expression/test)

