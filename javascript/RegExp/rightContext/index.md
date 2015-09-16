---
title: rightContext
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/b4sb5k1b(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Returns the characters from the position following the last match to the end of the searched string. Read-only.'
tags:
  - JS
  - Basic
uri: javascript/RegExp/rightContext

---
## Summary

Returns the characters from the position following the last match to the end of the searched string. Read-only.

## Syntax

<span class="language">JavaScript</span>

    RegExp.rightContext

## Examples

The following example illustrates the use of the **rightContext** property:

``` js
// Create the regular expression pattern.
    var re = new RegExp("d(b+)(d)","ig");
    var str = "cdbBdbsbdbdz";

    // Perform the search.
    var arr = re.exec(str);

    // Print the output.
    var s = ""
    s += ": " + RegExp. + "<br />";
    s += ": " + RegExp. + "<br />";
    s += ": " + RegExp. + "<br />";
    s += "input: " + RegExp.input + "<br />";
    s += "lastMatch: " + RegExp.lastMatch + "<br />";
    s += "leftContext: " + RegExp.leftContext + "<br />";
    s += "rightContext: " + RegExp.rightContext + "<br />";
    s += "lastParen: " + RegExp.lastParen + "<br />";

    document.write(s);
```

## Remarks

The object associated with this property is always the global **RegExp** object.

The initial value of the **rightContext** property is an empty string. The value of the **rightContext** property changes whenever a successful match is made.

## See also

### Other articles

-   [\$1...\$9 Properties (RegExp)](/javascript/RegExp/1_9_Properties)
-   [index Property (RegExp)](/javascript/RegExp/index)
-   [input Property (\$\_) (RegExp)](/javascript/RegExp/input)
-   [lastIndex Property (RegExp)](/javascript/RegExp/lastIndex)
-   [lastMatch Property (\$&) (RegExp)](/javascript/RegExp/lastMatch)
-   [lastParen Property (\$+) (RegExp)](/javascript/RegExp/lastParen)
-   [leftContext Property (\$\`) (RegExp)](/javascript/RegExp/leftContext)

