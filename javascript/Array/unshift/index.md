---
title: unshift
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/ezk94dwt(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Inserts new elements at the start of an array.'
tags:
  0: JS
  1: Basic
  3: Method
uri: javascript/Array/unshift

---
## Summary

Inserts new elements at the start of an array.

## Syntax

<span class="language">JavaScript</span>

    unshift([ item1 [, item2 [, . . . [, itemN]]]])

**item1, item2,. . ., itemN**
:   Optional. Elements to insert at the start of the **Array**.

## Examples

The following example illustrates the use of the unshift method.

``` js
var ar = new Array();
 ar.unshift(10, 11);
 ar.unshift(12, 13, 14);
 document.write(ar.toString());

 // Output: 12,13,14,10,11
```

## Remarks

The **unshift** method inserts elements into the start of an array, so they appear in the same order in which they appear in the argument list.

## See also

### Specification

[15.4.4.13 Array.prototype.unshift ( [ item1 [ , item2 [ , …](http://www.ecma-international.org/ecma-262/5.1/#sec-15.4.4.13) ] ] )] ECMAScript® Language Specification Standard ECMA-262 5.1 Edition / June 2011

