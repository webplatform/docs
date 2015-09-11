---
title: parseInt
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/x53yedee(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Converts a string to an integer.'
tags:
  - JS
  - Basic
uri: javascript/parseInt

---
## <span>Summary</span>

Converts a string to an integer.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    parseInt( numString , [ radix ])

**numString**
:   Required. A string to convert into a number.

**radix**
:   Optional. A value between 2 and 36 that specifies the base of the number in numString. If this argument is not supplied, strings with a prefix of '0x' are considered hexadecimal. All other strings are considered decimal.

## <span>Examples</span>

``` js
parseInt("123.45");  // returns 123
parseInt("abc");  // returns NaN
parseInt("12abc");  // returns 12
```

## <span>Remarks</span>

The **parseInt** function returns an integer value equal to the number contained in numString. If no prefix of numString can be successfully parsed into an integer, **NaN** (not a number) is returned.

You can test for **NaN** using the **isNaN** function.

## <span>See also</span>

### <span>Other articles</span>

-   [isNaN Function](/javascript/isNaN)
-   [parseFloat Function](/javascript/parseFloat)
-   [String Object](/javascript/String)
-   [valueOf Method (Object)](/javascript/Object/valueOf)

