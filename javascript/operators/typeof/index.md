---
title: 'typeof'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/259s7zc1(v=vs.94).aspx)'
compatibility:
  feature: typeof
  topic: javascript
readiness: 'Ready to Use'
summary: 'Returns a string that identifies the data type of an expression.'
tags:
  - JS_Basic
uri: javascript/operators/typeof

---
## Summary

Returns a string that identifies the data type of an expression.

## Syntax

    typeof [ ( ] expression [ ) ] ;

## Examples

The following example tests the data type of variables.

``` js
var index = 5;
 var result = (typeof index === 'number');
 // Output: true

 var description = "abc";
 var result = (typeof description === 'string');
 // Output: true
```

The following example tests for a data type of undefined for declared and undeclared variables.

``` js
var declared;
 var result = (declared === undefined);
 // Output: true

 var result = (typeof declared === 'undefined');
 // Output: true

 var result = (typeof notDeclared === 'undefined')
 // Output: true

 var obj = {};
 var result = (typeof obj.propNotDeclared === 'undefined');
 // Output: true

 // An undeclared variable cannot be compared to undefined,
 // so the next line generates an error.
 //  var result = (notDeclared === undefined);
```

## Remarks

The expression argument is any expression for which type information is sought.

The typeof operator returns type information as a string. There are six possible values that typeof returns: "number," "string," "boolean," "object," "function," and "undefined."

The parentheses are optional in the typeof syntax.

## See also

### Other articles

-   [Array.isArray Function](/javascript/Array/isArray)
-   [Object.getPrototypeOf Function](/javascript/Object/getPrototypeOf)
-   [undefined Constant](/javascript/undefined)
-   [Comparison Operators](/javascript/operators/comparison)

