---
title: 'width'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/Web/CSS/width)'
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://code.webplatform.org/gist/5702862'
compatibility:
  feature: width
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`auto`'
  'Applies to': 'All elements except inline, non-replaced elements, table rows, and row groups.'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'percentage or absolute length'
  Animatable: 'Yes'
  '[CSS Object Model Property](/css/concepts/cssom)': '`/css/cssom/properties/width`'
  Percentages: 'refer to width of containing block'
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Specifies the width of the content area of an element. The content area of the element width does not include the padding, border, and margin of the element.'
tags:
  - CSS_Properties
  - CSS
uri: css/properties/width

---
## Summary

Specifies the width of the content area of an element. The content area of the element width does not include the padding, border, and margin of the element.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `auto`

Applies to
:   All elements except inline, non-replaced elements, table rows, and row groups.

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   percentage or absolute length

Animatable
:   Yes

[CSS Object Model Property](/css/concepts/cssom)
:   `/css/cssom/properties/width`

Percentages
:   refer to width of containing block

## Syntax

-   `width: auto`
-   `width: available`
-   `width: border-box`
-   `width: content-box`
-   `width: fit-content`
-   `width: intrinsic`
-   `width: length`
-   `width: max-content`
-   `width: min-content`
-   `width: percentage`

## Values

auto
:   If auto is set for the elements width, the browser will determine the width for the element.

length
:   Will take a number that is immediately followed by a length unit such as px, em, in, etc.

percentage
:   Integer, followed by a %. The value is a percentage of the width of the parent object, whether or not it is specified explicitly. Negative values are not allowed.

border-box
:   If border-box is used, the length or percentage defined will be applied to the element's border box.

content-box
:   If content-box is used, the length or percentage defined will be applied to the element's content-box.

max-content
:   The intrinsic preferred width

min-content
:   The intrinsic minimum width

available
:   The containing block width minus horizontal margin, border, and padding

fit-content
:   This will be either the large of the minimum width or the smaller of the preferred width and the available width

intrinsic
:   This is an experimental rule for max-content. Currently it only works in Chrome, however you should be using max-content instead since that is the standard.

## Examples

``` css
div { width: 100% }
h1 { width: 20em }
section { width: auto }
img { width: 100px }
```

Example using new values that are part of the CSS Basic Box Model that is currently in working draft.

``` html
<style>
/* Width values of the CSS Box Model working draft */

div {
    box-sizing: border-box;
    border: 1px solid #444;
    width: 350px;
    margin: 5px;
}

p {
    background: #000;
    color: #fff;
    padding: 5px;
    font-family: Arial, sans-serif;
}

p.mincontent {
    /* vendor prefix needed */
    width: -webkit-min-content;
}

p.maxcontent {
    /* vendor prefix needed */
    width: -webkit-max-content;
}

p.fitcontent {
    /* vendor prefix needed */
    width: -webkit-fit-content;
}
</style>

<div>
<p>This is the content inside of the parent div.</p>
</div>

<div>
<p class="mincontent">This is the content inside of the parent div.</p>
<p class="mincontent">Min-content matches the widest single word like "Antidisestablishmentarianism".</p>
</div>

<div>
<p class="maxcontent">This is the content inside of the parent div. Max-content expands to fit the content.</p>
</div>

<div>
<p class="fitcontent">This fits the content inside of the parent div.</p>
</div>
```

[View live example](http://code.webplatform.org/gist/5702862)

## Usage

     ===Newer Values===

In the CSS Basic Box Model Working Draft, the values max-content, min-content, available, fit-content, border-box, and content-box were added. It would be a best practice to add the vendor prefix to these until the values are standardized.

## Related specifications

[CSS Basic Box Model](http://dev.w3.org/csswg/css-box/#the-width-and-height-properties)
:   Working Draft

[CSS Level 2](http://www.w3.org/TR/CSS2/visudet.html#the-width-property)
:   Recommendation

[CSS Level 1](http://www.w3.org/TR/CSS1/#width)
:   Recommendation

## See also

### External resources

-   <http://www.w3.org/TR/CSS2/visudet.html#the-width-property>
-   <http://www.w3.org/TR/CSS21/visudet.html#propdef-width>

### Related pages

-   CSSStyleDeclaration[CSSStyleDeclaration](/css/cssom/CSSStyleDeclaration/CSSStyleDeclaration)
-   currentStyle[currentStyle](/css/cssom/currentStyle)
-   runtimeStyle[runtimeStyle](/css/cssom/runtimeStyle)
-   style[style](/css/cssom/style)
-   `Conceptual`
-   `Measuring Element Dimension and Location with CSSOM in Internet Explorer 9`
-   `Other Resources`
-   `CSS Enhancements in Internet Explorer 6`
