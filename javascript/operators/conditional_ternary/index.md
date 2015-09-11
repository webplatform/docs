---
title: conditional ternary
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/be21c7hw(v=vs.94).aspx)'
readiness: 'Ready to Use'
summary: 'Returns one of two expressions depending on a condition. Also referred to as &quot;if...else shorthand&quot;.'
tags:
  - JS
  - Basic
uri: 'javascript/operators/conditional ternary'

---
## <span>Summary</span>

Returns one of two expressions depending on a condition. Also referred to as &quot;if...else shorthand&quot;.

## <span>Syntax</span>

<span class="language">JavaScript</span>

    test ? expression1 : expression2

**test**
:   Any Boolean expression.

**expression1**
:   An expression returned if test is true. May be a comma expression.

**expression2**
:   An expression returned if test is false. More than one expression may be a linked by a comma expression.

## <span>Examples</span>

The ?: operator can be used as a shortcut for an if...else statement. It is typically used as part of a larger expression where an if...else statement would be awkward. This example creates a string containing "Good evening." if it is after 6pm, or "Good day." otherwise.

``` js
var now = new Date();
var greeting = "Good" + ((now.getHours() > 17) ? " evening." : " day.");
```

The equivalent code using a regular if...else statement would look as follows:

``` js
var now = new Date();
var greeting = "Good";
if (now.getHours() > 17)
    greeting += " evening.";
else
    greeting += " day.";
```

## <span>See also</span>

### <span>Other articles</span>

-   [if...else Statement](/javascript/statements/if_else)

