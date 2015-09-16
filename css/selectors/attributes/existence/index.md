---
title: 'Attribute selector'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: existence
  topic: css
notes:
  - 'Needs summary, spec reference, standardization status, remove topic cluster flags'
readiness: 'In Progress'
standardization_status: 'W3C Recommendation'
summary: 'Allows to select tags that has an attributes. While it can match the class and the id selector, its specificity value is lower.'
tags:
  - CSS
  - Selectors
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - selection
uri: css/selectors/attributes/existence

---
## Summary

Allows to select tags that has an attributes. While it can match the class and the id selector, its specificity value is lower.

### Syntax

` [sel=att] {...}`

### Parameters

-   *sel*: The name of a tag property
-   *att*: Must be either an Identifier or a String.
-   "=": An equality expression, one of
    -   `=` Exactly equals,
    -   `^=` Begins with,
    -   `$=` Ends with,
    -   `~=` Contains (with word boundary),
    -   `*=` Contains (without word boundary)

## Examples

The following style rule selects any element with an "attr" attribute whose value is exactly "Value".

``` html
<!DOCTYPE html>
<html>
  <head>
    <style type="text/css">
      .test          { display:none; }
      [attr="Value"] { display:block; }
    </style>
  </head>
  <body>
    <div class="test" attr="Value">Test for [=] (Value) succeeded.</div>
  </body>
</html>
```

## Related specifications

[Selectors Level 3](http://www.w3.org/TR/css3-selectors/#attribute-selectors)
:   W3C Recommendation

## See also

### Related articles

#### CSS Attributes

-   [background-blend-mode](/css/properties/background-blend-mode)

-   [background-position](/css/properties/background-position)

-   [break-before](/css/properties/break-before)

-   [height](/css/properties/height)

-   [list-style](/css/properties/list-style)

-   [list-style-position](/css/properties/list-style-position)

-   [text-overflow-ellipsis](/css/properties/text-overflow-ellipsis)

-   [text-overflow-mode](/css/properties/text-overflow-mode)

-   [text-rendering](/css/properties/text-rendering)

-   [user-select](/css/properties/user-select)

-   [equality](/css/selectors/attributes/equality)

-   **Attribute selector**

-   [hyphen](/css/selectors/attributes/hyphen)

-   [prefix](/css/selectors/attributes/prefix)

-   [substring](/css/selectors/attributes/substring)

-   [suffix](/css/selectors/attributes/suffix)

-   [baseline-shift](/svg/attributes/baseline-shift)

-   [JavaScript animation](/tutorials/animation_in_javascript_2)

#### Selectors

-   [querySelectorAll](/css/selectors_api/querySelectorAll)

-   [ID](/css/selectors/ID)

-   [Namespaced](/css/selectors/Namespaced)

-   [Universal](/css/selectors/Universal)

-   [equality](/css/selectors/attributes/equality)

-   **Attribute selector**

-   [hyphen](/css/selectors/attributes/hyphen)

-   [prefix](/css/selectors/attributes/prefix)

-   [substring](/css/selectors/attributes/substring)

-   [suffix](/css/selectors/attributes/suffix)

-   [whitespace](/css/selectors/attributes/whitespace)

-   [:-ms-input-placeholder](/css/selectors/pseudo-classes/:-ms-input-placeholder)

-   [:checked](/css/selectors/pseudo-classes/:checked)

-   [:disabled](/css/selectors/pseudo-classes/:disabled)

-   [:empty](/css/selectors/pseudo-classes/:empty)

-   [:enabled](/css/selectors/pseudo-classes/:enabled)

-   [:first-child](/css/selectors/pseudo-classes/:first-child)

-   [:first-of-type](/css/selectors/pseudo-classes/:first-of-type)

-   [:focus](/css/selectors/pseudo-classes/:focus)

-   [:in-range](/css/selectors/pseudo-classes/:in-range)

-   [:indeterminate](/css/selectors/pseudo-classes/:indeterminate)

-   [:invalid](/css/selectors/pseudo-classes/:invalid)

-   [:lang(c)](/css/selectors/pseudo-classes/:lang(c))

-   [:last-of-type](/css/selectors/pseudo-classes/:last-of-type)

-   [:nth-child(n)](/css/selectors/pseudo-classes/:nth-child(n))

-   [:nth-last-child(n)](/css/selectors/pseudo-classes/:nth-last-child(n))

-   [:nth-last-of-type(n)](/css/selectors/pseudo-classes/:nth-last-of-type(n))

-   [:nth-of-type(n)](/css/selectors/pseudo-classes/:nth-of-type(n))

-   [:only-child](/css/selectors/pseudo-classes/:only-child)

-   [:only-of-type](/css/selectors/pseudo-classes/:only-of-type)

-   [:optional](/css/selectors/pseudo-classes/:optional)

-   [:required](/css/selectors/pseudo-classes/:required)

-   [:root](/css/selectors/pseudo-classes/:root)

-   [:target](/css/selectors/pseudo-classes/:target)

-   [:valid](/css/selectors/pseudo-classes/:valid)

-   [::selection](/w/index.php?title=selection&action=edit&redlink=1)

-   [type](/css/selectors/type)
