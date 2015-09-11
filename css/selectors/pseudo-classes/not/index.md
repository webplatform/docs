---
title: :not
tags:
  - CSS
uri: 'css/selectors/pseudo-classes/:not'

---
The negation pseudo-class, `:not(X)`, is a functional notation taking a [selector](http://www.w3.org/TR/2011/REC-css3-selectors-20110929/#simple-selectors-dfn%7Csimple) (excluding the negation pseudo-class itself) as an argument. It represents an element that is not represented by its argument.

Negations may not be nested; `:not(:not(...))` is invalid. Note also that since pseudo-elements are not simple selectors, they are not a valid argument to `:not()`.

## <span>Examples:</span>

The following selector matches all button elements in an HTML document that are not disabled.

``` css
button:not([DISABLED])
```

The following selector represents all but FOO elements.

``` css
*:not(FOO)
```

The following group of selectors represents all HTML elements except links.

``` css
html|*:not(:link):not(:visited)
```

 Default namespace declarations do not affect the argument of the negation pseudo-class unless the argument is a universal selector or a type selector.

Assuming that the default namespace is bound to "<http://example.com/>", the following selector represents all elements that are not in that namespace:

``` css
*|*:not(*)
```

The following selector matches any element that is not being hovered, regardless of its namespace. In particular, it is not limited to only matching elements in the default namespace that are not being hovered, and elements not in the default namespace don't match the rule when they are being hovered.

``` css
*|*:not(:hover)
```

> **Note:** the `:not()` pseudo allows useless selectors to be written. For instance `:not(*|*)`, which represents no element at all, or `foo:not(bar)`, which is equivalent to foo but with a higher specificity.