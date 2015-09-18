---
title: 'right'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/CSS/right)'
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://code.webplatform.org/gist/6181880'
compatibility:
  feature: right
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`auto`'
  'Applies to': 'All elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'If specified as a length, the corresponding absolute length; if specified as a percentage, the specified value; otherwise, ''auto''.'
  Animatable: 'Yes'
  '[CSS Object Model Property](/css/concepts/cssom)': '`right`'
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Specifies the position an element in relation to the right side of the containing element.'
tags:
  - CSS_Properties
  - CSS
uri: css/properties/right

---
## Summary

Specifies the position an element in relation to the right side of the containing element.

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
:   `right`

## Syntax

-   `right: auto`
-   `right: length`
-   `right: percentage`

## Values

auto
:   Default. Position is determined by the regular HTML layout of the page.

length
:   Floating-point number, followed by an absolute units designator (`cm`, `mm`, `in`, `pt`, or `pc`) or a relative units designator (`em`, `ex`, or `px`). For more information about the supported length units, see CSS Values and Units Reference.

percentage
:   Integer, followed by a percent sign (%). The value is a percentage of the width of the parent object.

## Examples

We demonstrate the \`right\` property by positioning the elements.

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
   * Offsets this element 50px to the left of the container's right edge.
   * Note: `length` can also be specified in other units of measurements.
   */
  right: 50px;
}

.absolutely-positioned-within-body {
  /**
   * Here, the nearest positioned anscestor does not exist, hence
   * the coordinate system reference becomes the initial containing block,
   * i.e. the `body`.
   */
  position: absolute;
  /**
   * Offsets this element 150px to the left of the initial containing
   * block's right edge i.e. the `body`'s right edge.
   */
  right: 150px;
}

.relatively-positioned {
  /**
   * Object is positioned according to the normal flow, and then offset.
   */
  position: relative;
  /**
   * The layout for this element happens according to the normal flow.
   * But because this element is positioned relatively, it will be
   * offset 30px towards the left from where it would have been in
   * the normal flow.
   */
  right: 30px;
}
```

[View live example](http://code.webplatform.org/gist/6181880)

The HTML for the above example.

``` html


<article>
  <div class="container">
    <p class="box absolutely-positioned-within-container">Absolutely positioned within <code>div.container</code> at 50px left from the container's right edge.</p>
    <p class="box relatively-positioned">This is relatively positioned at 30px from the right.</p>
  </div>

  <p class="box absolutely-positioned-within-body">This is absolutely positioned within the <code>body</code> at 150px to the left of the body's right edge.</p>
</article>
```

</pre>

## Related specifications

[CSS Visual Formatting Model](http://www.w3.org/TR/CSS2/visuren.html)
:   W3C Recommendation

## See also

### Related pages

-   CSSStyleDeclaration[CSSStyleDeclaration](/css/cssom/CSSStyleDeclaration/CSSStyleDeclaration)
-   currentStyle[currentStyle](/css/cssom/currentStyle)
-   `LayoutRect`
-   runtimeStyle[runtimeStyle](/css/cssom/runtimeStyle)
-   style[style](/css/cssom/style)
