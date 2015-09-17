---
title: 'background-attachment'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/background-attachment.htm'
compatibility:
  feature: background-attachment
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`scroll`'
  'Applies to': 'All elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'as specified'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`scroll`'
  Percentages: n/a
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Defines if a background image scrolls with the content or stays fixed.'
tags:
  - CSS_Properties
  - CSS
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/defaultSelected
uri: css/properties/background-attachment

---
## Summary

Defines if a background image scrolls with the content or stays fixed.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `scroll`

Applies to
:   All elements

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   as specified

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:   `scroll`

Percentages
:   n/a

## Syntax

-   `background-attachment: fixed`
-   `background-attachment: local`
-   `background-attachment: scroll`

## Values

scroll
:   Default. Background image scrolls with the object as the document is scrolled.

fixed
:   Background image stays fixed within the viewport and does not move when the element or the page is scrolled.

local
:   Background image stays fixed with regard to the element’s contents and scrolls as the element is scrolled.

## Examples

The following examples use the **background-attachment** attribute and the **background-attachment** property to set the background to "fixed", so that the background does not scroll with the text.

This example uses an inline style sheet to set the background to fixed.

``` html
<style >
    body { background-attachment:fixed }
</style>
</head>
<body background="some.jpg">
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/background-attachment.htm)

This example uses scripting to set the page background to fixed.

``` js
document.body.backgroundAttachment = 'fixed';
```

## Notes

### Remarks

This property can be set with the other background properties by using the [**background**](/css/cssom/properties/background) composite property.

With CSS3 Backgrounds, the background of a box can have multiple layers. The number of layers is determined by the number of comma-separated values in the [**background-image**](/css/properties/background-image) property. Each of the images is sized, positioned, and tiled according to the corresponding value in the other background properties (**background-attachment**, [**background-clip**](/css/properties/background-clip), [**background-origin**](/css/properties/background-origin), [**background-position**](/css/properties/background-position), [**background-repeat**](/css/properties/background-repeat), and [**background-size**](/css/properties/background-size)). The first image in the list is the layer closest to the user, the next one is painted behind the first, and so on.

## Related specifications

[CSS 2.1](http://www.w3.org/TR/CSS2/colors.html#propdef-background-attachment)
:   W3C Recommendation

[CSS Backgrounds and Borders Module Level 3](http://www.w3.org/TR/css3-background/#the-background-attachment)
:   W3C Candidate Recommendation

## See also

### Related articles

#### Background

-   [background](/css/cssom/properties/background)

-   [background](/css/properties/background)

-   **background-attachment**

-   [background-blend-mode](/css/properties/background-blend-mode)

-   [background-clip](/css/properties/background-clip)

-   [background-color](/css/properties/background-color)

-   [background-image](/css/properties/background-image)

-   [background-origin](/css/properties/background-origin)

-   [background-position](/css/properties/background-position)

-   [background-position-x](/css/properties/background-position-x)

-   [background-position-y](/css/properties/background-position-y)

-   [background-repeat](/css/properties/background-repeat)

-   [background-size](/css/properties/background-size)

-   [JavaScript animation](/tutorials/animation_in_javascript_2)

### Related pages

-   CSSStyleDeclaration[CSSStyleDeclaration](/css/cssom/CSSStyleDeclaration/CSSStyleDeclaration)
-   currentStyle[currentStyle](/css/cssom/currentStyle)
-   defaults[defaults](/w/index.php?title=dom/defaultSelected&action=edit&redlink=1)
-   `LayoutRect`
-   runtimeStyle[runtimeStyle](/css/cssom/runtimeStyle)
-   style[style](/css/cssom/style)
