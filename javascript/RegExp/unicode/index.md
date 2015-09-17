---
title: 'unicode'
code_samples:
  - 'https://mathiasbynens.be/notes/es6-unicode-regex#impact-dot'
compatibility:
  feature: unicode
  topic: javascript
notes:
  - 'Moved under javascript/RegExp'
readiness: 'Ready to Use'
summary: 'Returns a Boolean value indicating the state of the Unicode flag (u) used with a regular expression. Default is false. Read-only.'
tags:
  - JS_Basic
  - JS_Property
uri: javascript/RegExp/unicode

---
## Summary

Returns a Boolean value indicating the state of the Unicode flag (u) used with a regular expression. Default is false. Read-only.

## Syntax

    regex.unicode

## Examples

The following example illustrates the use of the Unicode property.

``` js
// https://mathiasbynens.be/notes/es6-unicode-regex#impact-dot
// Note: `𝌆` is U+1D306 TETRAGRAM FOR CENTRE, a supplementary Unicode symbol.
var string = 'a𝌆b';

console.log(/a.b/.unicode);
// → false

console.log(/a.b/.test(string));
// → false

console.log(/a.b/u.unicode);
// → true

console.log(/a.b/u.test(string));
// → true

var match = string.match(/a(.)b/u);
console.log(match[1]);
// → '𝌆'
```

[View live example](https://mathiasbynens.be/notes/es6-unicode-regex#impact-dot)

## Remarks

The `unicode` property returns `true` if the Unicode flag is set for a regular expression, and returns `false` if it is not.

The Unicode flag, when used, enables [various Unicode-related features for regular expressions](https://mathiasbynens.be/notes/es6-unicode-regex), such as the use of ES6 Unicode code point escapes (e.g. `/\u{1D306}/u`).

## See also

### Related articles

#### Javascript

-   [propertyName](/dom/TransitionEvent/propertyName)

-   [Number](/javascript/Number)

-   **unicode**

-   [future reserved words](/javascript/future_reserved_words)

### Other articles

-   [global Property (Regular Expression)](/javascript/regular_expression/global)
-   [ignoreCase Property (Regular Expression)](/javascript/regular_expression/ignoreCase)
-   [multiline Property (Regular Expression)](/javascript/regular_expression/multiline)
-   [sticky Property (Regular Expression)](/javascript/regular_expression/sticky)

### External resources

-   [Unicode-aware regular expressions in ECMAScript 6](https://mathiasbynens.be/notes/es6-unicode-regex)
-   [regexpu – a source code transpiler that enables the use of ES6 Unicode regular expressions in ES5](https://github.com/mathiasbynens/regexpu)
-   [Traceur REPL demo](https://google.github.io/traceur-compiler/demo/repl.html#%2F%2F%20Traceur%20now%20uses%20regexpu%20(https%3A%2F%2Fmths.be%2Fregexpu)%20to%20transpile%20regular%0A%2F%2F%20expression%20literals%20that%20have%20the%20ES6%20%60u%60%20flag%20set%20into%20equivalent%20ES5.%0A%0A%2F%2F%20Match%20any%20symbol%20from%20U%2B1F4A9%20PILE%20OF%20POO%20to%20U%2B1F4AB%20DIZZY%20SYMBOL.%0Avar%20regex%20%3D%20%2F%5B%F0%9F%92%A9-%F0%9F%92%AB%5D%2Fu%3B%20%2F%2F%20Or%2C%20%60%2F%5Cu%7B1F4A9%7D-%5Cu%7B1F4AB%7D%2Fu%60.%0Aconsole.log(%0A%20%20regex.test('%F0%9F%92%A8')%2C%20%2F%2F%20false%0A%20%20regex.test('%F0%9F%92%A9')%2C%20%2F%2F%20true%0A%20%20regex.test('%F0%9F%92%AA')%2C%20%2F%2F%20true%0A%20%20regex.test('%F0%9F%92%AB')%2C%20%2F%2F%20true%0A%20%20regex.test('%F0%9F%92%AC')%20%20%2F%2F%20false%0A)%3B%0A%0A%2F%2F%20See%20https%3A%2F%2Fmathiasbynens.be%2Fnotes%2Fes6-unicode-regex%20for%20more%20examples%20and%0A%2F%2F%20info.%0A)

