---
title: void
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/e17c7cbe(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'The void operator evaluates an expression and then returns undefined.'
tags:
  - JS
  - Basic
uri: javascript/operators/void

---
## Summary

The void operator evaluates an expression and then returns undefined.

## Syntax

<span class="language">JavaScript</span>

    void expression

## Examples

In this example, `void(0)` is used to return `undefined` to the link's `href` property, so that the browser will not attempt to load a URL and the function in the `onclick` event can be executed instead.

``` html
<!DOCTYPE html>
<html>
<head>
<title>JavaScript void example</title>
</head>
<body>
<a href="javascript:void(0)" onclick="myFunction()">Click here to execute the function.</a>
</body>
</html>
```

## Remarks

The expression argument is any valid JavaScript expression.

The void operator evaluates its expression and returns undefined. It is useful in situations where an expression should be evaluated but you do not want a result returned to the rest of the script.

Void works only on unary expressions, thus: ` void x, y; ` will set only the x variable to **undefined**.

## Notes

void(0) is equivalent to void 0 and returns the **undefined** value.

