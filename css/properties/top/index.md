---
title: top
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/6171243'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`auto`'
  'Applies to': 'Positioned elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'If specified as a length, the corresponding absolute length; if specified as a percentage, the specified value; otherwise, ''auto''.'
  Animatable: 'Yes'
  '[CSS Object Model Property](/css/concepts/cssom)': '`top`'
  Percentages: 'refer to height of containing block'
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'This property specifies how far an absolutely positioned box''s top margin edge is offset below the top edge of the box''s containing block. For relatively positioned boxes, the offset is with respect to the top edges of the box itself (i.e., the box is given a position in the normal flow, then offset from that position according to these properties).'
tags:
  - CSS
  - Properties
uri: css/properties/top

---
## <span>Summary</span>

This property specifies how far an absolutely positioned box's top margin edge is offset below the top edge of the box's containing block. For relatively positioned boxes, the offset is with respect to the top edges of the box itself (i.e., the box is given a position in the normal flow, then offset from that position according to these properties).

## <span>Overview table</span>

[Initial value](/css/concepts/initial_value)
:   `auto`

Applies to
:   Positioned elements

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   If specified as a length, the corresponding absolute length; if specified as a percentage, the specified value; otherwise, 'auto'.

Animatable
:   Yes

[CSS Object Model Property](/css/concepts/cssom)
:   `top`

Percentages
:   refer to height of containing block

## <span>Syntax</span>

-   `top: auto`
-   `top: length`
-   `top: percentage`

## <span>Values</span>

auto
:   For non-replaced elements, the effect of this value depends on which of related properties have the value 'auto' as well. See the sections on the width and height of absolutely positioned, non-replaced elements for details. For replaced elements, the effect of this value depends only on the intrinsic dimensions of the replaced content. See the sections on the width and height of absolutely positioned, replaced elements for details

length
:   The offset is a fixed distance from the reference edge. Negative values are allowed. For more information about the supported length units, see CSS Values and Units Reference.

percentage
:   The offset is a percentage of the containing block's width (for 'left' or 'right') or height (for 'top' and 'bottom'). Negative values are allowed.

## <span>Examples</span>

We demonstrate the \`top\` property by positioning the elements.

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
   * Offsets this element 25px below the container's top edge.
   * Note: `length` can also be specified in other units of measurements.
   */
  top: 25px;
}

.absolutely-positioned-within-body {
  /**
   * Here, the nearest positioned ancestor does not exist, hence
   * the coordinate system reference becomes the initial containing block,
   * i.e. the `body`.
   */
  position: absolute;
  /**
   * Offsets this element 350px below the initial containing block's top edge,
   * i.e. the `body`.
   */
  top: 350px;
}

.relatively-positioned {
  /**
   * Object is positioned according to the normal flow, and then offset.
   */
  position: relative;
  /**
   * The layout for this element happens according to the normal flow.
   * But because this element is positioned relatively, it will be
   * offset 100px below from where it would have been in the normal flow.
   */
  top: 100px;
}
```

[View live example](http://code.webplatform.org/gist/6171243)

The HTML for the above example.

``` html


<article>
  <div class="container">
    <p class="box absolutely-positioned-within-container">Absolutely positioned within <code>div.container</code> at 25px from the top.</p>
    <p class="box relatively-positioned">This is relatively positioned at 100px from the top.</p>
  </div>

  <p class="box absolutely-positioned-within-body">This is absolutely positioned within the <code>body</code> at 350px from the top.</p>
</article>
```

</pre>

## <span>Related specifications</span>

[Cascading Style Sheets Level 2 Revision 1 (CSS 2.1) Specification](http://www.w3.org/TR/2007/CR-CSS21-20070719/visuren.html#position-props)
:   Recommendation
