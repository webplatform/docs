---
title: toString
tags:
  0: JS
  1: Basic
  3: Method
readiness: 'Ready to Use'
summary: 'Returns a string representation of a Boolean object.'
uri: javascript/Boolean/toString

---
# toString

## Summary

Returns a string representation of a Boolean object.

## Syntax

    boolean.toString()

**boolean**
:   Required. An object for which to get a string representation.

## Return Value

If the Boolean value is true , returns "true". Otherwise, returns "false".

## Examples

The following example illustrates the use of the **toString** method.

``` {.js}
var s = new Boolean(0);
 document.write(s.toString());

 // Output: false;
```

Create a Boolean variable and convert it to a string

``` {.js}
// Create a Boolean Variable
var flag = new Boolean(true);
// Convert the variable to a string
var myVar = flag.toString();
// myVar returns the string "true"
```

## See also

### Specification

[Boolean Objects](http://www.ecma-international.org/ecma-262/5.1/#sec-15.6) ECMAScript® Language Specification Standard ECMA-262 5.1 Edition / June 2011

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/jj155292(v=vs.94).aspx)

