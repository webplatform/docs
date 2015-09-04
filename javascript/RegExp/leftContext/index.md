---
title: leftContext
tags:
  - JS
  - Basic
readiness: 'Ready to Use'
summary: 'Returns the characters from the beginning of a searched string up to the position before the beginning of the last match. Read-only.'
uri: javascript/RegExp/leftContext

---
# leftContext

## Summary

Returns the characters from the beginning of a searched string up to the position before the beginning of the last match. Read-only.

## Syntax

    RegExp.leftContext

## Examples

The following example illustrates the use of the **leftContext** property:

``` {.js}
// Create the regular expression pattern.
    var re = new RegExp("d(b+)(d)","ig");
    var str = "cdbBdbsbdbdz";

    // Perform the search.
    var arr = re.exec(str);

    // Print the output.
    var s = ""
    s += "$1: " + RegExp.$1 + "<br />";
    s += "$2: " + RegExp.$2 + "<br />";
    s += "$3: " + RegExp.$3 + "<br />";
    s += "input: " + RegExp.input + "<br />";
    s += "lastMatch: " + RegExp.lastMatch + "<br />";
    s += "leftContext: " + RegExp.leftContext + "<br />";
    s += "rightContext: " + RegExp.rightContext + "<br />";
    s += "lastParen: " + RegExp.lastParen + "<br />";

    document.write(s);
```

## Remarks

The object associated with this property is always the global **RegExp** object.

The initial value of the **leftContext** property is an empty string. The value of the **leftContext** property changes whenever a successful match is made.

## See also

### Other articles

-   [\$1...\$9 Properties (RegExp)](/javascript/RegExp/1_9_Properties)
-   [index Property (RegExp)](/javascript/RegExp/index)
-   [input Property (\$\_) (RegExp)](/javascript/RegExp/input)
-   [lastIndex Property (RegExp)](/javascript/RegExp/lastIndex)
-   [lastMatch Property (\$&) (RegExp)](/javascript/RegExp/lastMatch)
-   [lastParen Property (\$+) (RegExp)](/javascript/RegExp/lastParen)
-   [rightContext Property (\$') (RegExp)](/javascript/RegExp/rightContext)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/0ch447h1(v=vs.94).aspx)

