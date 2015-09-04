---
title: input
tags:
  - JS
  - Basic
readiness: 'Ready to Use'
summary: 'Returns the string against which a regular expression search was performed. Read-only.'
uri: javascript/RegExp/input

---
# input

## Summary

Returns the string against which a regular expression search was performed. Read-only.

## Syntax

    RegExp.input

## Examples

The object associated with this property is always the global **RegExp** object.

The value of **input** property is modified any time the searched string is changed.

The following example illustrates the use of the **input** property:

``` {.js}
function inputDemo() {
    var s;
    var re = new RegExp("d(b+)(d)","ig");
    var str = "cdbBdbsbdbdz";
    var arr = re.exec(str);
    s = "The string used for the match was " + RegExp.input ;
    return(s);
}
```

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/dsa56hkc(v=vs.94).aspx)

