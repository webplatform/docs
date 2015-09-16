---
title: sticky
notes:
  - 'Moved under javascript/RegExp'
readiness: 'Ready to Use'
summary: 'Returns a Boolean value indicating the state of the sticky flag ( y ) used with a regular expression. Default is false. Read-only.'
tags:
  0: JS
  1: Basic
  3: Property
uri: javascript/RegExp/sticky

---
## Summary

Returns a Boolean value indicating the state of the sticky flag ( y ) used with a regular expression. Default is false. Read-only.

## Syntax

    regex.sticky

## Examples

The following example illustrates the use of the `sticky` property.

``` js
var regex = /foo.bar/gy;
regex.sticky;
// → true
regex.lastIndex;
// → 0

regex.test('foo*bar');
// → true
regex.lastIndex;
// → 7
regex.test('..foo*bar');
// → false

regex.lastIndex = 0;
regex.test('..foo*bar');
// → false

regex.lastIndex = 2;
regex.test('..foo*bar');
// → true
regex.lastIndex;
// → 9
```

## Remarks

The `sticky` property returns `true` if the sticky flag is set for a regular expression, and returns `false` if it is not.

The `sticky` flag, when used, indicates that the regular expression performs sticky matching in the target string by attempting to match starting at `lastIndex`. If matching at that location fails, then `null` is returned, i.e., no forward “anchoring” search is performed. If matching succeeds, then the regular expression’s `lastIndex` property is updated as for the flag `g`.

## See also

### Other articles

-   [global Property (Regular Expression)](/javascript/regular_expression/global)
-   [ignoreCase Property (Regular Expression)](/javascript/regular_expression/ignoreCase)
-   [multiline Property (Regular Expression)](/javascript/regular_expression/multiline)
-   [unicode Property (Regular Expression)](/javascript/regular_expression/unicode)

