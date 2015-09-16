---
title: pointer-events
code_samples:
  - 'http://jsbin.com/uvumuj/3'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`auto`'
  'Applies to': 'all elements'
  '[Inherited](/css/concepts/inherited)': 'Yes'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'the specified value'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`pointerEvents`'
readiness: 'Ready to Use'
summary: 'The pointer-events property  allows you to control whether an element can be the target for the pointing device (e.g, mouse, pen) events.'
tags:
  0: CSS
  1: Properties
  3: SVG
uri: css/properties/pointer-events

---
## Summary

The pointer-events property allows you to control whether an element can be the target for the pointing device (e.g, mouse, pen) events.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `auto`

Applies to
:   all elements

[Inherited](/css/concepts/inherited)
:   Yes

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   the specified value

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:   `pointerEvents`

## Syntax

-   `pointer-events: all`
-   `pointer-events: auto`
-   `pointer-events: fill`
-   `pointer-events: none`
-   `pointer-events: painted`
-   `pointer-events: stroke`
-   `pointer-events: visible`
-   `pointer-events: visibleFill`
-   `pointer-events: visiblePainted`
-   `pointer-events: visibleStroke`

## Values

auto
:   In HTML/XML content, this value and the value all have the same effect. In SVG content, this value and the value visiblePainted have the same effect.

none
:   The element is never the target of pointer events, although pointer events may target its descendant elements if those descendants have the `pointer-events` set to some other value.

all
:   The element may be the target element for pointer events whenever the pointer is inside the CSS border edge of the element.

visiblePainted
:   For SVG only. The element can only be the target of a pointer event when the `visibility` property is set to <span class="value">visible</span> and when the pointer is over the interior (i.e., 'fill') of the element or the perimeter (i.e., 'stroke') of the element, and the `fill`, `stroke` property is set to a value other than none.

visibleFill
:   For SVG only. The element can only be the target of a pointer event when the `visibility` property is set to visible and when the pointer is over the interior (i.e., fill) of the element.

visibleStroke
:   For SVG only. The element can only be the target of a pointer event when the `visibility` property is set to visible and when the pointer is over the perimeter (i.e., stroke) of the element.

visible
:   The element may be the target of pointer events when the `visibility` property is set to visible, and the pointer is over the contents, background, or border of the element (or in SVG, over either the interior (i.e., fill) or the perimeter (i.e., stroke) of the element).

painted
:   For SVG only. The element can only be the target of a pointer event when the pointer is over the interior (i.e., 'fill') of the element or the perimeter (i.e., 'stroke') of the element, and the `fill`, `stroke` property is set to a value other than none.

fill
:   For SVG only. The element can only be the target of a pointer event when the pointer is over the interior (i.e., fill) of the element.

stroke
:   For SVG only. The element can only be the target of a pointer event when the pointer is over the perimeter (i.e., stroke) of the element.

## Examples

The first a element have the pointer-events property set to none, any pointer events (i.e., mouse over, click) do not happen.

``` html
<!DOCTYPE HTML>
<html lang="en-US">
<head>
  <meta charset="UTF-8">
  <title>Pointer-events example</title>
  <link href="pointer-events.css" type="text/css" rel="stylesheet">
</head>
<body>

  <p><a href="http://docs.webplatform.org" id="one">webplatform.org(none)</a></p>
  <p><a href="http://docs.webplatform.org" id="two">webplatform.org(all)</a></p>

</body>
</html>
```

``` css
#one{
  pointer-events: none;
}
#two{
  pointer-events: all;
}
```

SVG demo of two intersecting circles

``` html
{see jsbin for the full source}
```

[View live example](http://jsbin.com/uvumuj/3)

## Notes

The pointer-events property used to be in the CSS 3 UI specification, but it has been postponed to CSS 4 due to many open issues.

## Related specifications

[Scalable Vector Graphics (SVG) 1.1 (Second Edition)](http://www.w3.org/TR/SVG11/interact.html#PointerEventsProperty)
:   W3C Recommendation

Note: The pointer-events property used to be in the CSS 3 UI specification, but it has been postponed to CSS 4 due to many open issues.
