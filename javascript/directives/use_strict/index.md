---
title: 'use strict'
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer JavaScript reference Article](http://msdn.microsoft.com/en-us/library/ie/yek4tbz0%28v=vs.94%29.aspx)'
compatibility:
  feature: 'use strict'
  topic: javascript
readiness: 'Ready to Use'
summary: 'Restricts the use of some potentially-harmful features of JavaScript (e.g., eval, with) and throws syntax errors for certain sloppy code.'
tags:
  - JS_Basic
uri: 'javascript/directives/use strict'

---
## Summary

Restricts the use of some potentially-harmful features of JavaScript (e.g., eval, with) and throws syntax errors for certain sloppy code.

## Syntax

    "use strict";

## Examples

The following code causes a syntax error because in strict mode all variables must be declared with `var`.

``` js
// Be careful - all code used in the page/context must be strict mode conformant.
"use strict";
function testFunction(){
   var testvar = 4;
    return testvar;
}
intvar = testFunction();
```

The following code causes a syntax error because in strict mode all variables must be declared with `var`. Even though the strict mode directive (`use strict;`) is only added to the function, the whole code breaks because that function does not adhere to the strict mode rules.

``` js
function testFunction(){
   // Restricts strict mode to this function only.
   "use strict";
   // This will throw.
   testvar = 4;
   return testvar;
}
var hello = true;
```

The following code \_does not\_ cause a syntax error, even though the variable **intvar** variable is not declared with `var`, because the strict mode is scoped to the function only, while the non conformant code is found in a different scope (the global scope).

``` js
function testFunction(){
   // Restricts strict mode to this function only.
   "use strict";
   var testvar = 4;
   return testvar;
}

// This would have caused a syntax error to be thrown if there had been
// a "use strict"; directive at the top of the script (above the testFunction
// function). Since the directive is scoped to the function and not to the
// global scope (in which this code operates), this code runs normally.
intvar = 1;
```

When the expression `"use strict";` is placed at the start of a script or a function body, the code contained in it is parsed under stricter rules than what the default JavaScript language allows. These rules include:

-   Variables must be explicitly declared (`var`).
-   Statements must end with a semicolon (`;`).
-   Assigning values to a read-only property fails (`Node.DOCUMENT_FRAGMENT_NODE = 9;`).
-   **with** statements are completely disallowed.

**TODO**: Add the complete set of strict mode rules.

