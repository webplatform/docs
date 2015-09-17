---
title: 'regular expression'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/h6e2eb7w(v=vs.94).aspx)'
compatibility:
  feature: 'regular expression'
  topic: javascript
notes:
  - 'Dup of javascript/RegExp; deletion candidate.'
readiness: 'Not Ready'
summary: 'An object that contains a regular expression pattern along with flags that identify how to apply the pattern.'
tags:
  - JS_Basic
  - JS_Object
uri: 'javascript/regular expression'

---
## Summary

An object that contains a regular expression pattern along with flags that identify how to apply the pattern.

## Syntax

    re = / pattern / [ flags ]
    re = new RegExp(" pattern " [ ," flags " ] )

**re**
:   Required. The variable name to which the regular expression pattern is assigned.

**pattern**
:   Required. The regular expression pattern to use. If you use Syntax 1, delimit the pattern by "/" characters. If you use Syntax 2, enclose the pattern in quotation marks.

**flags**
:   Optional. Enclose flag in quotation marks if you use Syntax 2. Available flags, which may be combined, are: g (global search for all occurrences of pattern ) i (ignore case) m (multiline search) y (sticky) u (Unicode)

## Examples

The following example illustrates the use of the **Regular Expression** object by creating an object (re) containing a regular expression pattern with its associated flags. In this case, the resulting **Regular Expression** object is then used by the **match** method:

``` js
function MatchDemo(){
    var s = "through the pages of the book";

 // Create regular expression pattern.
    var re = new RegExp("the", "i");

 // Attempt match on search string.
    var r = s.match(re);

 // Return first occurrence of "the".
    return(r);
 }
```

## Remarks

The **Regular Expression** object should not be confused with the global **RegExp** object. Even though they sound the same, they are separate and distinct. The properties of the **Regular Expression** object contain only information about one particular **Regular Expression** instance, while the properties of the global **RegExp** object contain continually updated information about each match as it occurs.

**Regular Expression** objects store patterns used when searching strings for character combinations. After the **Regular Expression** object is created, it is either passed to a string method, or a string is passed to one of the regular expression methods. Information about the most recent search performed is stored in the global **RegExp** object.

Use Syntax 1 when you know the search string ahead of time. Use Syntax 2 when the search string is changing frequently, or is unknown, such as strings taken from user input.

The pattern argument is compiled into an internal format before use. For Syntax 1, pattern is compiled as the script is loaded. For Syntax 2, pattern is compiled just before use, or when the **compile** method is called.

## Properties

The following table lists the properties of the **regular expression** object.

## Functions

The following table lists the functions of the **regular expression** object.

## Methods

The following table lists the methods of the **regular expression** object.

## See also

### Other articles

-   [RegExp Object](/javascript/RegExp)
-   [String Object](/javascript/String)

