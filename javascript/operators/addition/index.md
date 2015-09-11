---
title: addition
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/wwfws59w(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Adds the value of one numeric expression to another, or concatenates two strings.'
tags:
  - JS
  - Basic
uri: javascript/operators/addition

---
## <span>Summary</span>

Adds the value of one numeric expression to another, or concatenates two strings.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    result = expression1 + expression2;

**result**
:   Any variable.

**expression1**
:   Any expression.

**expression2**
:   Any expression.

## <span>Examples</span>

``` js
console.log(1 + 1); // 2
console.log('hello' + ' world'); // 'hello world'
console.log(1 + '1'); // '11'
console.log('1' + 1); // '11'
```

## <span>Remarks</span>

The types of the two expressions determine the behavior of the `+` operator.

|If|Then|
|:--|:---|
|Both expressions are numeric or Boolean|Add|
|Both expressions are strings|Concatenate|
|One expression is numeric and the other is a string|Concatenate|

## <span>See also</span>

### <span>Other articles</span>

-   [Addition Assignment Operator (`+=`)](/javascript/operators/addition_assignment)

