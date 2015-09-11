---
title: undefined
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/dae3sbk5(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'A value that has never been defined, such as a variable that has not been initialized.'
tags:
  - JS
  - Basic
uri: javascript/undefined

---
## <span>Summary</span>

A value that has never been defined, such as a variable that has not been initialized.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    undefined

## <span>Examples</span>

Usage of **undefined** with strict equality.

``` js
var foo;

if (foo === undefined) {
    // executes
} else {
   // won't execute
}
```

Usage of `undefined` with the [typeof operator](/javascript/operators/typeof).

``` js
var foo;

if (typeof foo === 'undefined') {
    // executes
} else {
   // won't execute
}
```

Comparison of strict equality and the [typeof operator](/javascript/operators/typeof). `typeof` doesn’t throw an error if the variable hasn’t been defined, because its value is implicitly `undefined`.

``` js
// foo variable is not defined
if (typeof foo === "undefined") {
    // executes
}

if (foo === undefined) {
    // throws ReferenceError
}
```

## <span>Remarks</span>

The `undefined` constant is a member of the **Global** object, and becomes available when the scripting engine is initialized. When a variable has been declared but not initialized, its value is `undefined`.

If a variable has not been declared, you cannot compare it to `undefined` , but you can compare the type of the variable to the string `"undefined"`. (see second example)

The `undefined` constant is useful when explicitly testing or setting a variable to `undefined`.

## <span>Usage</span>

     undefined is not a reserved word, thus can be used as a variable in any scope except for the global scope.

## <span>Notes</span>

## <span>**undefined** vs. **null**</span>

**undefined** means a value is declared but not initialized, it doesn't have a value assigned to it.

[null](/javascript/null) can be assigned to a variable to represent no value.

Other than that, `undefined` is a type, while `null` is an object

## <span>See also</span>

### <span>Other articles</span>

-   [typeof Operator](/javascript/operators/typeof)

