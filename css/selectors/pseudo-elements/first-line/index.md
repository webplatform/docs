---
title: ::first-line
tags:
  - CSS
  - Selectors
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Represents the first line of an element. Note that the content of the first line varies depending on the available width and the styling of text (size, spacing).'
code_samples:
  - 'https://gist.github.com/fe1382a764e07a9c7917'
uri: 'css/selectors/pseudo-elements/::first-line'

---
# ::first-line

## Summary

Represents the first line of an element. Note that the content of the first line varies depending on the available width and the styling of text (size, spacing).

### Syntax

``` {.css}
::first-line {}
```

### Usage

The ::first-line pseudo-element can be attached to block-level elements. It can be attached to inline elements if you set the corresponding display property to block.

## Examples

The following example puts the first line of any paragraph in bold text

``` {.css}
p::first-line {
    font-weight: bold;
}
```

[View live example](https://code.webplatform.org/gist/fe1382a764e07a9c7917)

## Notes

### Remarks

Only the following properties apply to the ::first-letter pseudo-element: [**background**](/css/properties/background), [**clear**](/css/properties/clear), [**color**](/css/properties/color), [**font**](/css/properties/font), [**font-family**](/css/properties/font-family), [**font-size**](/css/properties/font-size), [**font-style**](/css/properties/font-style), [**font-variant**](/css/fonts/font-variant), [**font-weight**](/css/properties/font-weight), [**line-height**](/css/properties/line-height), [**text-decoration**](/css/properties/text-decoration), [**text-transform**](/css/properties/text-transform), [**vertical-align**](/css/properties/vertical-align), and [**word-spacing**](/css/text/word-spacing/word-spacing)

## Related specifications

Specification
:   Status
[W3C CSS 2.1 Selectors](http://www.w3.org/TR/CSS2/selector.html#first-line-pseudo)
:   W3C Recommendation
[W3C CSS Selectors Level 3](http://www.w3.org/TR/css3-selectors/#first-line)
:   W3C Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network.

