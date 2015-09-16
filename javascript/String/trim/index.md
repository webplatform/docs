---
title: trim
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/ff679971(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Removes the leading and trailing white space and line terminator characters from a string.'
tags:
  - JS
  - Basic
uri: javascript/String/trim

---
## Summary

Removes the leading and trailing white space and line terminator characters from a string.

## Syntax

<span class="language">JavaScript</span>

    stringObj.trim()

**stringObj**
:   Required. A String object or string literal. This string is not modified by the **trim** method.

## Return Value

The original string with leading and trailing white space and line terminator characters removed.

## Examples

The following example illustrates the use of the **trim** method.

``` js
var message = "    abc def     \r\n  ";

 document.write("[" + message.trim() + "]");
 document.write("<br/>");
 document.write("length: " + message.trim().length);

 // Output:
 //  [abc def]
 //  length: 7
```

## Remarks

The characters that are removed include space, tab, form feed, carriage return, and line feed. See Special Characters (Windows Scripting - JScript) for a comprehensive list of white space and line terminator characters.

For an example that shows how to implement your own trim method, see Prototypes and Prototype Inheritance.

## See also

### Other articles

-   [String Object](/javascript/String)

