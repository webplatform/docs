---
title: NaN
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/z2bz9h52(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'A special constant that specifies a value that is Not-A-Number'
tags:
  - JS
  - Basic
uri: javascript/NaN

---
## <span>Summary</span>

A special constant that specifies a value that is Not-A-Number

## <span>Syntax</span>

<span class="language">JavaScript</span>

    NaN

## <span>Examples</span>

**NaN** mainly occurs when parsing goes wrong

``` js
parseInt(123); // 123
parseInt("123"); // 123
parseInt('foo'); // NaN
```

**NaN** does not equal **NaN**, use the [isNaN Function](/javascript/isNaN) instead to test if a value is not a number

``` js
NaN === NaN; // false
isNaN(NaN); //true
```

## <span>Remarks</span>

The **NaN** constant is a member of the **Global** object, and is made available when the scripting engine is initialized.

## <span>See also</span>

### <span>Other articles</span>

-   [isNaN Function](/javascript/isNaN)
-   [Number](/javascript/Number)
-   [Number Constants](/javascript/Number/constants)
-   [parseInt Function](/javascript/parseInt)

