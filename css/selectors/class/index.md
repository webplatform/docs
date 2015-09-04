---
title: class
tags:
  - CSS
  - Selectors
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Styles all elements with the specified class.'
uri: css/selectors/class

---
# class

## Summary

Styles all elements with the specified class.

## Examples

For example, the following style rule matches any [p](/html/elements/p) element whose class attribute has been assigned a space-separated list of values that include the "pastoral" and "marine" class names. This rule matches when class="pastoral aqua marine" but does not match when class="pastoral blue".

``` {.css}
<style>
    p.pastoral.marine { color: lightseagreen; }
</style>
```

## Notes

### Remarks

The class attribute value must immediately follow the "period" (.) notation. More than one class name can be specified in one style rule; to match a subset of class values, each value must be preceded by a period.

### Syntax

`<strong/>sel.value {...}`

### Parameters

*sel*
:   Selector
*value*
:   String that specifies the value of the "class" attribute.

### Standards information

-   [CSS 2.1](http://go.microsoft.com/fwlink/p/?linkid=203757), Section 1.4

## Related specifications

Specification
:   Status
[CSS Level 2 Specification](http://www.w3.org/TR/CSS2/)
:   W3C Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

