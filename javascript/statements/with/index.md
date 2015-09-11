---
title: with
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/b294afx9(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Establishes the default object for a statement. Disallowed in strict mode.'
tags:
  - JS
  - Basic
uri: javascript/statements/with

---
## <span>Summary</span>

Establishes the default object for a statement. Disallowed in strict mode.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    with ( object ) {
         statements
    }

**object**
:   The new default object.

**statements**
:   One or more statements for which object is the default object.

## <span>Examples</span>

The with statement is commonly used to shorten the amount of code that you have to write in certain situations. In this example, notice the repeated use of Math.

When you use the **with** statement, your code may become shorter and easier to read (yet with uncommon semantics).

``` js
// Not using 'with'.
var x = Math.cos(3 * Math.PI) + Math.sin(Math.LN10);
var y = Math.tan(14 * Math.E);

// Using 'with'.
var x, y;
with (Math) {
    x = cos(3 * PI) + sin (LN10);
    y = tan(14 * E);
}
```

The following strict mode code will cause a syntax error to be thrown, because **with** statements are disallowed in strict mode.

``` js
"use strict";
with (Math) {
    console.log(cos(3));
}
```

This statement changes the default context from a global or a function scope, to one of a given context. Every variable declared within the body of this statement (within the curly brackets) is defined on the given context instead of on the function or global scope.

 This statement is disallowed in [strict mode](/javascript/directives/use_strict) and so will generate a syntax error before even running the script.

## <span>See also</span>

### <span>Other articles</span>

-   [this Statement](/javascript/statements/this)

