---
title: 'touch-action'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/library/ie/hh772044.aspx)'
code_samples:
  - 'http://www.love2dev.com/'
compatibility:
  feature: touch-action
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`auto`'
  'Applies to': 'All elements except non-replaced inline elements, table rows, row groups, table columns, and column groups'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'Same as specified value'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
  Percentages: N/A
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Determines whether touch input may trigger default behavior supplied by the user agent, such as panning or zooming.'
tags:
  - CSS
  - Properties
uri: css/properties/touch-action

---
## Summary

Determines whether touch input may trigger default behavior supplied by the user agent, such as panning or zooming.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `auto`

Applies to
:   All elements except non-replaced inline elements, table rows, row groups, table columns, and column groups

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   Same as specified value

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:

Percentages
:   N/A

## Syntax

-   `touch-action: auto`
-   `touch-action: manipulation`
-   `touch-action: none`
-   `touch-action: pan-x`
-   `touch-action: pan-y`

## Values

auto
:   The user agent MAY determine any permitted touch behaviors, such as panning and zooming manipulations of the viewport, for touches that begin on the element.

none
:   Touches that begin on the element MUST NOT trigger default touch behaviors.

pan-x
:   The user agent MAY consider touches that begin on the element only for the purposes of horizontally scrolling the element's nearest ancestor with horizontally scrollable content.

pan-y
:   The user agent MAY consider touches that begin on the element only for the purposes of vertically scrolling the element's nearest ancestor with vertically scrollable content.

manipulation
:   The user agent MAY consider touches that begin on the element only for the purposes of scrolling and continuous zooming.

## Examples

You might find the following example within a fingerpainting application to ensure that its canvas doesn't move when a user touches and manipulates it. When a user touches this canvas and moves his or her finger, no manipulation will occur. DOM events will be sent instead.

``` css
canvas#fingerpainter {
  touch-action: none;
}
```

The application has content that extends horizontally beyond the viewport and the desired behavior is to allow the user to scroll content left and right as desired without the browser moving the entire page.

``` html
<div style="touch-action: pan-x;">
    This element receives pointer events when not panning in the horizontal direction.
</div>
```

[View live example](http://www.love2dev.com/)

## Related specifications

[Pointer Events](https://dvcs.w3.org/hg/pointerevents/raw-file/tip/pointerEvents.html#the-touch-action-css-property)
:   Editor's Draft

