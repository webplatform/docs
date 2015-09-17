---
title: 'overflow-style'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: overflow-style
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`auto`'
  'Applies to': 'non-replaced block-level elements and non-replaced inline-block elements'
  '[Inherited](/css/concepts/inherited)': 'Yes'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'as specified'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`overflowStyle`'
  Percentages: n/a
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Specifies the preferred scrolling methods for elements that overflow.'
tags:
  - CSS_Properties
  - CSS
uri: css/properties/overflow-style

---
## Summary

Specifies the preferred scrolling methods for elements that overflow.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `auto`

Applies to
:   non-replaced block-level elements and non-replaced inline-block elements

[Inherited](/css/concepts/inherited)
:   Yes

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   as specified

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:   `overflowStyle`

Percentages
:   n/a

## Syntax

-   `overflow-style: auto`
-   `overflow-style: marquee`
-   `overflow-style: move`
-   `overflow-style: none`
-   `overflow-style: panner`
-   `overflow-style: scrollbar`

## Values

auto
:   Initial value. Indicates no preference.

none
:   Indicates the element does not display any scrolling mechanism, even when its content overflows.

Unlike [**overflow**](/css/properties/overflow): **hidden**, elements with **overflow-style**: **none** can still be scrolled via touch panning, keyboard, or mouse wheel.

scrollbar
:   Indicates the element displays a classic scrollbar-type control when its content overflows.

Scrollbars do not overlay content, and therefore take up extra layout space along the edges of the element where they appear.

panner
:   A panner is typically a rectangle shown in one corner of the element, with a smaller rectangle inside. The larger rectangle represents all the available content of the element and the smaller one the visible part. The smaller rectangle can be moved around by the user to move the content of the element accordingly.

move
:   The value ‘move’ refers to a method where the user can move the content of the element directly (rather than indirectly by moving a scrollbar or a panner). Typically, the mouse pointer changes into a hand or a cross of four arrows to indicate that the user can drag the content around with the mouse. Sometimes the user needs to explicitly activate the move mode and in that case he often can use both dragging (with the mouse) and key events to move the content.

marquee
:   The marquee effect (value ‘marquee’) consists of the content moving autonomously, without any user events to control it. A user who waits long enough will eventually see all the content that overflows.

## Examples

``` css
/* Top preference for a scrolling mechanism is a panner.
   If not available no visible scrolling mechanism should be displayed */
overflow-style: panner, none;
```

## Notes

## IMPORTANT

CSS Basic Box Model and CSS Marquee Module Lelel 3 both specify a different overflow-style property. This page is based on the CSS Basic Box Model, because if marquee is going to be supported, that would have a bigger chance of being supported.

### Remarks

The **overflow-style** property only has an effect on elements that overflow using the [**overflow**](/css/properties/overflow) property. When using auto-hiding scrollbars, you should ensure your content has sufficient padding to prevent interactive content from being obscured beneath the scrollbar.

## Related specifications

[CSS Basic Box Model](http://www.w3.org/TR/css3-box/#the-lsquo3)
:   Working Draft

[CSS Marquee Module Level 3](http://www.w3.org/TR/2008/WD-css3-marquee-20080801/#the-overflow-style)
:   Working Draft
