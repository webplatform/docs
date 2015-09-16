---
title: 'z-index'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/Web/CSS/z-index)'
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
code_samples:
  - 'http://gist.github.com/6199316'
  - 'http://gist.github.com/6199504'
  - 'http://gist.github.com/6199565'
compatibility:
  feature: z-index
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`auto`'
  'Applies to': 'Positioned elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'As specified'
  Animatable: 'Yes'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
  Percentages: N/A
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'The z-index property controls the stacking order of elements. As the x-axis defines the horizontal (left-right) position of elements on the screen, and the y-axis defines the vertical (top-down) position, think of the z-axis as the third dimension or depth-of-field, rising “out of” the screen, towards the viewer, or descending “into” the screen, away from the viewer.'
tags:
  - CSS
  - Properties
uri: css/properties/z-index

---
## Summary

The z-index property controls the stacking order of elements. As the x-axis defines the horizontal (left-right) position of elements on the screen, and the y-axis defines the vertical (top-down) position, think of the z-axis as the third dimension or depth-of-field, rising “out of” the screen, towards the viewer, or descending “into” the screen, away from the viewer.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `auto`

Applies to
:   Positioned elements

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   As specified

Animatable
:   Yes

[CSS Object Model Property](/css/concepts/cssom)
:

Percentages
:   N/A

## Syntax

-   `z-index: <integer>`
-   `z-index: auto`
-   `z-index: inherit`

## Values

auto
:   Default. Specifies the stacking order of the positioned objects based on the top-down order in which the objects appear in the HTML source.

\<integer\>
:   Integer that specifies the position of the object in the stacking order. The value is arbitrary and may be negative, zero, or positive.

inherit
:   Takes the same specified value as the property for the element's parent.

## Examples

The following example demonstrates the `z-index` property set to `auto`. Some style rules have been omitted for brevity. Please see the live example to view all the style rules.

``` css
.box {
  /**
   * The elements with the class `.box` are positioned absolutely
   * so as to make them overlap on each other. This helps demonstrate
   * the z-index property easily.
   */
  position: absolute;
  /**
   * The stacking order (z-index) is set to auto. Thus, the elements
   * stack in the order in which they appear in the DOM.
   */
  z-index: auto;
}

/* We offset the elements a little so the stacking order is easily seen. */
.bottom {
  top: 50px;
  left: 50px;
}

.middle {
  top: 100px;
  left: 60px;
}

.top {
  top: 150px;
  left: 70px;
}
```

[View live example](http://code.webplatform.org/gist/6199316)

``` html


<div class="container">
    <div class="box bottom">This box is at the bottom with z-index set to auto.</div>
    <div class="box middle">This box is in the middle with z-index set to auto.</div>
    <div class="box top">This box is at the top with z-index set to auto.</div>
</div>
```

</pre>

The following example demonstrates the `z-index` property set to an integer. Some style rules have been omitted for brevity. Please see the live example to view all the style rules.

``` css
.box {
  /**
   * The elements with the class `.box` are positioned absolutely
   * so as to make them overlap on each other. This helps demonstrate
   * the z-index property easily.
   */
  position: absolute;
}

/* We offset the elements a little so the stacking order is easily seen. */
.bottom {
  top: 10px;
  left: 50px;
  /**
   * The stacking order position of this element is 10.
   */
  z-index: 10;
}

.middle-level-one {
  top: 60px;
  left: 60px;
  /**
   * The stacking order position of this element is greater than
   * that of `div.bottom`, thus this element will appear above `div.bottom`.
   */
  z-index: 20;
}

.middle-level-two {
  top: 120px;
  left: 70px;
  /**
   * The stacking order of this element is same as that of `div.middle-level-one`.
   * Thus, these two elements will follow DOM order.
   */
  z-index: 20;
}

.top {
  top: 180px;
  left: 80px;
  /**
   * The stacking order of this element is greater than all the other elements.
   * Thus this element will appear above all of them.
   */
  z-index: 30;
}
```

[View live example](http://code.webplatform.org/gist/6199504)

``` html


<div class="container">
    <div class="box top">This box is at the top with z-index set to 30.</div>
    <div class="box middle-level-one">This box is in the middle level 1 with z-index set to 20.</div>
    <div class="box middle-level-two">This box is in at middle level 2 with z-index set to 20.</div>
    <div class="box bottom">This box is at the bottom with z-index set to 10.</div>
</div>
```

</pre>

The following example demonstrates the `z-index` property set to `inherit`. Some style rules have been omitted for brevity. Please see the live example to view all the style rules.

``` css
.box {
  /**
   * The elements with the class `.box` are positioned absolutely
   * so as to make them overlap on each other. This helps demonstrate
   * the z-index property easily.
   */
  position: absolute;
}

/* We offset the elements a little so the stacking order is easily seen. */
.bottom {
  top: 10px;
  left: 50px;
  /**
   * The stacking order position of this element is 10.
   */
  z-index: 10;
}

.middle {
  top: 60px;
  left: 60px;
  /**
   * The stacking order position of this element is greater than
   * that of `div.bottom`, thus this element will appear above `div.bottom`.
   */
  z-index: 20;
}

.middle-child {
  /**
   * The stacking order of this element is inherited from its parent, `div.middle`.
   * Thus, this will have the same stacking order as its parent.
   */
  z-index: inherit;
}

.top {
  top: 130px;
  left: 80px;
  /**
   * The stacking order of this element is greater than all the other elements.
   * Thus this element will appear above all of them.
   */
  z-index: 30;
}
```

[View live example](http://code.webplatform.org/gist/6199565)

``` html


<div class="container">
  <div class="box top">This box is at the top with z-index set to 30.</div>
  <div class="box middle">
    <div class="box middle-child">This box is the child of <code>div.middle</code> with z-index set to inherit.</div>
  </div>
  <div class="box bottom">This box is at the bottom with z-index set to 10.</div>
</div>
```

</pre>

## Usage

     The z-index property controls the “z” dimension dimension, stacking (layering) elements above or below others. Elements with a higher z-index appear closer to the viewer and overlap other elements in the same space, whereas a lower z-index makes them appear behind other elements, occupying the same space on the cartesian plane. Different browsers have different interpretations of z-index ordering, so beware.

Remember that elements that are overlapped in this way are reachable by keyboard users and screen readers, which usually is confusing. Consider hiding (using `display:none;`) any completely invisible elements.

This property only works with elements that are positioned **absolute**, **relative**, or **fixed**.

## Notes

If two objects have the same **z-index**, they’re stacked according to their source order.

An element with a positive z-index will be placed above an element that does not have a defined z-index. An element with a negative z-index will be placed below an element with no defined z-index.

The property does not apply to windowed controls, such as **select** objects.

When elements overlap, only the topmost element can receive action from a pointing device such as a mouse, even if it has a set opacity or is made invisible through CSS. This is also true for positioned elements with a negative z-index, unless:

-   the parent is a scrolling container (that is, its [overflow](/css/properties/overflow) property is set to **auto** or **scroll**), or
-   the parent is positioned (that is, its [position](/css/properties/position) property is set to **absolute**, **relative**, or **fixed**).

## Related specifications

[Visual formatting model](http://www.w3.org/TR/CSS2/visuren.html#propdef-z-index)
:   Recommendation

## See also

### External resources

-   <http://www.w3.org/TR/CSS2/visuren.html#z-index>
-   <https://developer.mozilla.org/en-US/docs/Web/CSS/z-index>

### Related pages

-   CSSStyleDeclaration[CSSStyleDeclaration](/css/cssom/CSSStyleDeclaration/CSSStyleDeclaration)
-   currentStyle[currentStyle](/css/cssom/currentStyle)
-   runtimeStyle[runtimeStyle](/css/cssom/runtimeStyle)
-   style[style](/css/cssom/style)
