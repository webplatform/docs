---
title: lastParen
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/x4bh3xk2(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Returns the last parenthesized submatch from any regular expression search, if any. Read-only.'
tags:
  - JS
  - Basic
uri: javascript/RegExp/lastParen

---
## <span>Summary</span>

Returns the last parenthesized submatch from any regular expression search, if any. Read-only.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    RegExp.lastParen

## <span>Examples</span>

The following example illustrates the use of the **lastParen** property:

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

## <span>Remarks</span>

The object associated with this property is always the global **RegExp** object.

The initial value of the **lastParen** property is an empty string. The value of the **lastParen** property changes whenever a successful match is made.

## <span>See also</span>

### <span>Other articles</span>

-   [\$1...\$9 Properties (RegExp)](/javascript/RegExp/1_9_Properties)
-   [index Property (RegExp)](/javascript/RegExp/index)
-   [input Property (\$\_) (RegExp)](/javascript/RegExp/input)
-   [lastIndex Property (RegExp)](/javascript/RegExp/lastIndex)
-   [lastMatch Property (\$&) (RegExp)](/javascript/RegExp/lastMatch)
-   [leftContext Property (\$\`) (RegExp)](/javascript/RegExp/leftContext)
-   [rightContext Property (\$') (RegExp)](/javascript/RegExp/rightContext)

