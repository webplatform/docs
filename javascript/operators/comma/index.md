---
title: comma
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/9b37css7(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'The comma operator (,) causes two expressions to be executed sequentially.'
tags:
  - JS
  - Basic
uri: javascript/operators/comma

---
## <span>Summary</span>

The comma operator (,) causes two expressions to be executed sequentially.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    expression1 , expression2

**expression1**
:   Any expression.

**expression2**
:   Any expression.

## <span>Examples</span>

The **,** operator causes the expressions to be executed in left-to-right order. A common use for the **,** operator is in the increment expression of a **for** loop. For example, the **for** statement allows only a single expression to be executed at the end of every pass through a loop. The **,** operator allows multiple expressions to be treated as a single expression, so both variables can be incremented.

``` js
j=25;
for (i = 0; i < 10; i++, j++)
{
    k = i + j;
}
```

## <span>See also</span>

### <span>Other articles</span>

-   [for Statement](/javascript/statements/for)

