---
title: 'left'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/6181854'
compatibility:
  feature: left
  topic: css
notes:
  - 'Add description, specifications, compatibility.'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`auto`'
  'Applies to': 'All elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'If specified as a length, the corresponding absolute length; if specified as a percentage, the specified value; otherwise, ''auto''.'
  Animatable: 'Yes'
  '[CSS Object Model Property](/css/concepts/cssom)': '`left`'
readiness: 'In Progress'
summary: 'Sets the left edge of an element'
tags:
  - CSS_Properties
  - CSS
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/defaultSelected
uri: css/properties/left

---
## Summary

Sets the left edge of an element

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
:   `left`

## Syntax

-   `left: auto`
-   `left: length`
-   `left: percentage`

## Values

auto
:   Default. Default position, according to the regular HTML layout of the page.

length
:   Floating-point number, followed by an absolute units designator (`cm`, `mm`, `in`, `pt`, or `pc`) or a relative units designator (`em`, `ex`, or `px`). For more information about the supported length units, see CSS Values and Units Reference.

percentage
:   Integer, followed by a percent sign (%). The value is a percentage of the width of the parent object.

## Examples

We demonstrate the \`left\` property by positioning the elements.

``` css
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
   * Here, the nearest positioned ancestor is the `div.container`.
   */
  position: absolute;
  /**
   * Offsets this element 25px towards the left from the container's left edge.
   * Note: `length` can also be specified in other units of measurements.
   */
  left: 25px;
}

.absolutely-positioned-within-body {
  /**
   * Here, the nearest positioned anscestor does not exist, hence
   * the coordinate system reference becomes the initial containing block,
   * i.e. the `body`.
   */
  position: absolute;
  /**
   * Offsets this element 350px towards the left of the initial containing
   * block's left edge i.e. the `body`'s left edge.
   */
  left: 350px;
}

.relatively-positioned {
  /**
   * Object is positioned according to the normal flow, and then offset.
   */
  position: relative;
  /**
   * The layout for this element happens according to the normal flow.
   * But because this element is positioned relatively, it will be
   * offset 300px towards the left from where it would have been in
   * the normal flow.
   */
  left: 300px;
}
```

[View live example](http://gist.github.com/6181854)

The HTML for the above example.

``` html


<article>
  <div class="container">
    <p class="box absolutely-positioned-within-container">Absolutely positioned within <code>div.container</code> at 25px from the left.</p>
    <p class="box relatively-positioned">This is relatively positioned at 300px from the left.</p>
  </div>

  <p class="box absolutely-positioned-within-body">This is absolutely positioned within the <code>body</code> at 350px from the left.</p>
</article>
```

</pre>

## See also

### Related articles

#### Box Model

-   [border](/css/properties/border)

-   [border-corner-shape](/css/properties/border-corner-shape)

-   [bottom](/css/properties/bottom)

-   [box-shadow](/css/properties/box-shadow)

-   [box-sizing](/css/properties/box-sizing)

-   [break-before](/css/properties/break-before)

-   [clear](/css/properties/clear)

-   [float](/css/properties/float)

-   [height](/css/properties/height)

-   **left**

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

### Related pages

-   CSSStyleDeclaration[CSSStyleDeclaration](/css/cssom/CSSStyleDeclaration/CSSStyleDeclaration)
-   currentStyle[currentStyle](/css/cssom/currentStyle)
-   defaults[defaults](/w/index.php?title=dom/defaultSelected&action=edit&redlink=1)
-   runtimeStyle[runtimeStyle](/css/cssom/runtimeStyle)
-   style[style](/css/cssom/style)
