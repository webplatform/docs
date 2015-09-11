---
title: Infinity
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/kddt5x39(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'A number that is larger than the largest floating point number.'
tags:
  - JS
  - Basic
uri: javascript/Infinity

---
## <span>Summary</span>

A number that is larger than the largest floating point number.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    Infinity

## <span>Return Value</span>

Returns an initial value of **Number.POSITIVE\_INFINITY**.

## <span>Examples</span>

Divisions by zero will give you Infinity. Divisions by negative zero will give you -Infinity.

``` js
42 / 0; // Infinity
42 / 0; // -Infinity
```

Everything beyond Infinity remains Infinity

``` js
Infinity * Infinity; // Infinity
```

If an arithmetic overflow occurs, Infinity is also returned

``` js
Math.pow(2, 1024); // Infinity
```

## <span>Remarks</span>

The **Infinity** constant is a member of the **Global** object, and is made available when the scripting engine is initialized.

## <span>Notes</span>

## <span>Negative Infinity</span>

Negative Infinity (-Infinity) is smaller than the smallest floating point number and returns a value of **Number.NEGATIVE\_INFINITY**.

## <span>Mathematical</span>

This value behaves mathematically like infinity; for example, anything multiplied by Infinity is Infinity, and anything divided by Infinity is 0.

Infinity subtracted by Infinity will return **NaN**

## <span>isFinite()</span>

The [isFinite()](/javascript/isFinite) function can be used to check if a given value is a finite number

## <span>See also</span>

### <span>Other articles</span>

-   [Number](/javascript/Number)
-   [Number Constants](/javascript/Number/constants)
-   [isFinite()](/javascript/isFinite)

