---
title: @namespace
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Empty "Main Content" section, see @import for notes for improvement suggestion. I haven''t come across @namespaces often in single-site implementations; perhaps we can provide elaboration on when @namespaces provide utility.'
readiness: 'In Progress'
standardization_status: 'W3C Recommendation'
summary: 'Declares the default namespace and binds a namespace to a namespace prefix.'
tags:
  - CSS
  - At
  - Rules
uri: css/atrules/@namespace

---
## Summary

Declares the default namespace and binds a namespace to a namespace prefix.

## Examples

The default namespace is applied to names that do not have an explicit namespace component. The following rule declares a default namespace.

``` html
@namespace "http://www.w3.org/1999/xhtml";
```

If you declare an **@namespace** rule with a prefix, you can use the prefix in namespace-qualified names. For example, consider the following namespace declaration for a namespace `prfx`.

``` html
@namespace prfx "http://prfx.contoso.com";
```

Based on the previous declaration, the following selector matches `E` elements in the namespace that the `prfx` prefix refers to.

``` html
prfx|E
```

The following code example creates two namespace prefixes. First, `p` elements in any namespace are colored red. Any `p` elements in the `prfx` namespace are then recolored blue, and `p` elements in the `msft` namespace are recolored green.

``` html
@namespace prfx "http://prfx.contoso.com";
@namespace msft "http://msft.example.com";
 p {background-color:red;}
prfx|p {background-color:blue;}
msft|p {background-color:green;}
```

The following code example styles a SVG element. By using the namespace and declaration from this example, all circles that are created with SVG are given a red fill.

``` html
@namespace svg "http://www.w3.org/2000/svg";
svg|circle {fill:red;}
```

## Notes

### Remarks

The **@namespace** rule was introduced in Windows Internet Explorer 9. The scope of an **@namespace** rule is the style sheet that it is declared in. You must declare an **@namespace** rule after any [**@charset**](/css/atrules/@charset) or [**@import**](/css/atrules/@import) rules.

### Syntax

`@namespace prfx? sUrl`

### Parameters

*prfx*
:   Optional. A **String** value that specifies a namespace prefix.
*sUrl*
:   A URL **String**value that specifies a namespace name.

## Related specifications

[CSS Namespaces Module](http://www.w3.org/TR/css3-namespace/#declaration)
:   W3C Recommendation

## See also

### Related articles

#### Syntax

-   [@charset](/css/atrules/@charset)

-   [@font-face](/css/atrules/@font-face)

-   [@import](/css/atrules/@import)

-   [@keyframes](/css/atrules/@keyframes)

-   **@namespace**

-   [@page](/css/atrules/@page)

-   [@supports](/css/atrules/@supports)

-   [CSS reference](/css/reference)

-   [Alphabetical list of CSS reference](/css/reference/alphabetical)

-   [!important](/css/syntax/!important)
