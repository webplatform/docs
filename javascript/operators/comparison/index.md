---
title: comparison
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/ky6fyhws(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Returns a Boolean value indicating the result of the comparison.'
tags:
  - JS
  - Basic
uri: javascript/operators/comparison

---
## <span>Summary</span>

Returns a Boolean value indicating the result of the comparison.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    expression1 comparisonoperator expression2

**expression1**
:   Any expression.

**comparisonoperator**
:   Any comparison operator (see Remarks).

**expression2**
:   Any expression.

## <span>Examples</span>

See Remarks.

``` js
var x = 5;
var y = 7;
var z = (x > y); // false
var z = (x < y); // true
var z = (y >= x); // true
var z = (y <= x); // false
```

## <span>Remarks</span>

When comparing strings, JavaScript uses the Unicode character value of the string expression.

The following describes how the different groups of operators behave depending on the types and values of expression1 and expression2 :

Relational operators: **\<** , **\>** , **\<=** , **\>=**

-   Attempt to convert both expression1 and expression2 into numbers.
-   If both expressions are strings, do a string comparison.
-   If either expression is **NaN** , return false.
-   Negative zero equals Positive zero.
-   Negative Infinity is less than everything including itself.
-   Positive Infinity is greater than everything including itself.

Equality operators: **==** , **!=**

-   If the types of the two expressions are different, attempt to convert them to a String, Number, or Boolean.
-   **NaN** is not equal to anything including itself.
-   Negative zero equals positive zero.
-   null equals both null and undefined.
-   Values are considered equal if they are identical strings, numerically equivalent numbers, the same object, identical Boolean values, or (if different types) they can be coerced into one of these situations.
-   Every other comparison is considered unequal.

Identity operators: **===** , **!==**

These operators behave the same as the equality operators, except that no type conversion is done. If the types of both expressions are not the same, these expressions always return false.

