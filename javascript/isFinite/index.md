---
title: isFinite
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/h5s8dazc(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Determines whether a supplied number is finite.'
tags:
  - JS
  - Basic
uri: javascript/isFinite

---
## <span>Summary</span>

Determines whether a supplied number is finite.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    isFinite(number)

**number**
:   Required. Any numeric value

## <span>Return Value</span>

Returns true if *number* is any value other than **NaN**, -Infinity or Infinity. In those three cases, it returns **false**.

## <span>Examples</span>

``` js
isFinite(); // false, because its NaN
isFinite(42); // true
isFinite(-Infinity); //false
isFinite(4 / 0); //false
```

## <span>See also</span>

### <span>Other articles</span>

-   [isNaN Function](/javascript/isNaN)
-   [Infinity](/javascript/Infinity)
-   [NaN](/javascript/NaN)

