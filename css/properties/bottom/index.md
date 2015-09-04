---
title: bottom
tags:
  - CSS
  - Properties
readiness: 'In Progress'
notes:
  - 'Add description, compatibility.'
summary: 'Sets the position of the bottom edge of an element.'
code_samples:
  - 'http://gist.github.com/6181867'
uri: css/properties/bottom
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/defaultSelected

---
# bottom

## Summary

Sets the position of the bottom edge of an element.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `auto`
Applies to
:   All elements
[Inherited](/css/concepts/inherited)
:   No
Media
:   visual
[Computed value](/css/concepts/computed_value)
:   If specified as a length, the corresponding absolute length; if specified as a percentage, the specified value; otherwise, 'auto'.
Animatable
:   Yes
[CSS Object Model Property](/css/concepts/cssom)
:   `bottom`

## Syntax

-   `bottom: auto`
-   `bottom: length`
-   `bottom: percentage`

## Values

auto
:   Default. Default position, according to the regular HTML layout of the page.

length
:   Floating-point number, followed by an absolute units designator (`cm`, `mm`, `in`, `pt`, or `pc`) or a relative units designator (`em`, `ex`, or `px`). For more information about the supported length units, see CSS Values and Units Reference.

percentage
:   Integer, followed by a percent sign (%). The value is a percentage of the height of the parent object.

## Examples

We demonstrate the \`bottom\` property by positioning these elements.

``` {.css}
.container {
  /**
   * Object is positioned according to the normal flow, and then offset.
   */
  position: relative;
}

.absolutely-positioned-within-container {
  /**
   * Object is positioned relative to nearest positioned ancestor—or
   * to the initial containing block if no positioned ancestor exists.
   * Here, the nearest positioned ancestor is the `<div class="container"^gt;`.
   */
  position: absolute;
  /**
   * Offsets this element 50px above the container's bottom edge.
   * Note: `length` can also be specified in other units of measurements.
   */
  bottom: 50px;
}

.absolutely-positioned-within-body {
  /**
   * Here, the nearest positioned anscestor does not exist, hence
   * the coordinate system reference becomes the initial containing block,
   * i.e. the `<body>`.
   */
  position: absolute;
  /**
   * Offsets this element 100px above the initial containing
   * block's bottom edge i.e. the `<body>`'s bottom edge.
   */
  bottom: 100px;
}

.relatively-positioned {
  /**
   * Object is positioned according to the normal flow, and then offset.
   */
  position: relative;
  /**
   * The layout for this element happens according to the normal flow.
   * But because this element is positioned relatively, it will be
   * offset 20px towards the left from where it would have been in
   * the normal flow.
   */
  bottom: 20px;
}
```

[View live example](http://code.webplatform.org/gist/6181867)

The HTML for the above example.

``` {.html}


<article>
  <div class="container">
    <p class="box absolutely-positioned-within-container">Absolutely positioned within <code>div.container</code> at 50px above the bottom edge.</p>
    <p class="box relatively-positioned">This is relatively positioned at 20px from the bottom.</p>
  </div>

  <p class="box absolutely-positioned-within-body">This is absolutely positioned within the <code>body</code> at 50px above the bottom edge.</p>
</article>
```

</pre>

## Related specifications

Specification
:   Status
[CSS 2.1, Visual formatting model](http://www.w3.org/TR/CSS2/visuren.html#propdef-bottom)
:   W3C Recommendation

## See also

### Related articles

#### Box Model

-   [border](/css/properties/border)

-   [border-corner-shape](/css/properties/border-corner-shape)

-   **bottom**

-   [box-shadow](/css/properties/box-shadow)

-   [box-sizing](/css/properties/box-sizing)

-   [break-before](/css/properties/break-before)

-   [clear](/css/properties/clear)

-   [float](/css/properties/float)

-   [height](/css/properties/height)

-   [left](/css/properties/left)

-   [line-height](/css/properties/line-height)

-   [margin](/css/properties/margin)

-   [margin-bottom](/css/properties/margin-bottom)

-   [margin-left](/css/properties/margin-left)

-   [margin-right](/css/properties/margin-right)

-   [margin-top](/css/properties/margin-top)

-   [max-height](/css/properties/max-height)

-   [max-width](/css/properties/max-width)

-   [min-height](/css/properties/min-height)

-   [min-width](/css/properties/min-width)

### Related pages (MSDN)

-   `CSSStyleDeclaration`
-   `currentStyle`
-   `defaults`
-   `runtimeStyle`
-   `style`
-   `Reference`
-   `pixelTop`
-   `posTop`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

