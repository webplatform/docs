---
title: :active
tags:
  - CSS
  - Selectors
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: "The\_:active pseudo-class applies while an element is being activated by the user."
uri: 'css/selectors/pseudo-classes/:active'
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/TouchEvent/touchstart

---
# :active

## Summary

The :active pseudo-class applies while an element is being activated by the user.

 The :active pseudo-class applies while an element is being activated by the user. For example, between the times the user presses the mouse button and releases it. On systems with more than one mouse button, :active applies only to the primary or primary activation button (typically the "left" mouse button), and any aliases thereof.

## Examples

The following style rule uses the **:active** pseudo-class to set the [**font-weight**](/css/properties/font-weight) and [**color**](/css/properties/color) attributes of an active link in a document.

``` {.css}
a:active { font-weight:bold; color:purple }
```

## Usage

     The :active pseudo-class is most often used with the a element.

The **:active** pseudo-class is often used with [**:hover**](/css/selectors/pseudo-classes/:hover), [**:link**](/css/selectors/pseudo-classes/:link), and [**:visited**](/css/selectors/pseudo-classes/:visited), the pseudo-classes that affect the other states of a link.

## Notes

It is undefined if the parent of an element that is ‘:active’ or ‘:hover’ is also in that state.

The default value of the **:active** pseudo-class is browser-specific.

By default, Safari Mobile does not use the **:active** state unless there is a [`touchstart`](/w/index.php?title=dom/TouchEvent/touchstart&action=edit&redlink=1) event handler on the relevant element or on the [`body`](/html/elements/body).

## Related specifications

Specification
:   Status
[CSS 2.1](http://www.w3.org/TR/CSS2/selector.html#dynamic-pseudo-classes)
:   W3C Recommendation
[Selectors Level 3](http://www.w3.org/TR/css3-selectors/#the-user-action-pseudo-classes-hover-act)
:   W3C Recommendation
[Selectors Level 4](http://dev.w3.org/csswg/selectors4/#active-pseudo)
:   W3C Working Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

