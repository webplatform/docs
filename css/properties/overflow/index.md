---
title: 'overflow'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/Web/CSS/overflow)'
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://code.webplatform.org/gist/6365118'
  - 'http://code.webplatform.org/gist/6365403'
  - 'http://code.webplatform.org/gist/6366211'
compatibility:
  feature: overflow
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`visible`'
  'Applies to': 'non-replaced block-level elements and non-replaced ’inline-block’ elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'as specified, except ‘visible’'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`overflow`'
readiness: 'Ready to Use'
standardization_status: Mixed
summary: 'The overflow property controls how extra content exceeding the bounding box of an element is rendered. It can be used in conjunction with an element that has a fixed width and height, to eliminate text-induced page distortion.'
tags:
  - CSS_Properties
  - CSS
uri: css/properties/overflow

---
## Summary

The overflow property controls how extra content exceeding the bounding box of an element is rendered. It can be used in conjunction with an element that has a fixed width and height, to eliminate text-induced page distortion.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `visible`

Applies to
:   non-replaced block-level elements and non-replaced ’inline-block’ elements

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   as specified, except ‘visible’

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:   `overflow`

## Syntax

-   `overflow: <overflow-x> <overflow-y>`
-   `overflow: auto`
-   `overflow: hidden`
-   `overflow: no-content`
-   `overflow: no-display`
-   `overflow: scroll`
-   `overflow: visible`

## Values

visible
:   The default value for most elements. Content is not clipped and a scroll mechanism is not added.

scroll
:   Content is clipped and a scroll mechanism is added, even if the content does not exceed the dimensions of the object.

hidden
:   Content that exceeds the dimensions of the object is not shown. No scroll mechanism is applied.

auto
:   Content is clipped and scrolling is added only when necessary.

no-display
:   When the content doesn't fit in the content box, the whole box is removed, as if ‘display: none’ were specified.

no-content
:   When the content doesn't fit in the content box, the whole content is hidden, as if ‘visibility: hidden’ were specified.

\<overflow-x\> \<overflow-y\>
:   Set **overflow-x** and **overflow-y** separately.

## Examples

Add different behavior for paragraphs via the `overflow` property.

``` css
.hidden {
    overflow: hidden;
}
.scroll {
    overflow: scroll;
}
.auto {
    overflow: auto;
}
.visible {
    overflow: visible;
}

/* Helper for paragraphes */
p {
    height: 60px;
}
```

[View live example](http://code.webplatform.org/gist/6365118)

Clearing floats with overflow

``` css
.clear {
    overflow: hidden;
    background: green;
}

/* A floating element that is bigger than its non-floating neighbor */
.floating {
    float: left;
    width: 200px;
}
```

[View live example](http://code.webplatform.org/gist/6365403)

Two values for `overflow`.

``` css
.overflow-y {
    overflow: hidden auto;
    height: 30px;
}
```

[View live example](http://code.webplatform.org/gist/6366211)

## Usage

     The overflow CSS property specifies whether to clip content, render scroll bars or display overflow content of a block-level element.

The `overflow` property takes up to two values. If given one value, both `overflow-x` and `overflow-y` are set to that value. If given two values, the first value applies to `overflow-x` and the second applies to `overflow-y`.

Using the overflow property with a value different than visible, its default, will create a new block formatting context. This is technically necessary as if a float would intersect with the scrolling element it would force to rewrap the content of the scrollable element around intruding floats. The rewrap would happen after each scroll step and would be lead to a far too slow scrolling experience. Note that, by programmatically setting scrollTop to the relevant HTML element, even when overflow has the hidden value an element may need to scroll.

## Notes

The default value for the `html` element is `auto`. Setting the `overflow` property to `visible` causes the content to clip to the size of the window or frame that contains the object.

### CSS basic box model

Specifying two values is currently not supported by browsers.

### Firefox (Gecko) Notes

Through Firefox 3.6 (Gecko 1.9.2), the overflow property is incorrectly applied to table-group elements (\<thead\> , \<tbody\> , \<tfoot\>). This behavior is corrected in later versions.

### Internet Explorer Notes

Internet Explorer 4 to 6 enlarges an element with `overflow: visible` (default value) to fit the content in it. height/width behaves like min-height/min-width.

-   [CSS 2.1](http://go.microsoft.com/fwlink/p/?linkid=203757), Section 11.1.1

## Related specifications

[CSS Level 2 (Revision 1)](http://www.w3.org/TR/CSS2/visufx.html#overflow)
:   Recommendation

[CSS3 module: The box model](http://www.w3.org/TR/2002/WD-css3-box-20021024/#overflow)
:   Working Draft

[CSS basic box model](http://www.w3.org/TR/css3-box/#overflow1)
:   Working Draft

## See also

### Related Properties

-   [overflow-x](/css/properties/overflow-x)
-   [overflow-y](/css/properties/overflow-y)
