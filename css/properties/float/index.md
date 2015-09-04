---
title: float
tags:
  - CSS
  - Properties
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Elements which have the style float  are floated horizontally.  These elements can move as far to the  left or right  of the containing element.  All elements after the floating element will flow around it, but elements before the floating element are not impacted.  If several floating elements are placed after each other, they will float next to each other as long as there is room.'
code_samples:
  - 'http://gist.github.com/5974883'
uri: css/properties/float
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/defaultSelected

---
# float

## Summary

Elements which have the style float are floated horizontally. These elements can move as far to the left or right of the containing element. All elements after the floating element will flow around it, but elements before the floating element are not impacted. If several floating elements are placed after each other, they will float next to each other as long as there is room.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `none`
Applies to
:   all elements except absolutely positioned, replaced elements
[Inherited](/css/concepts/inherited)
:   No
Media
:   visual
[Computed value](/css/concepts/computed_value)
:   as specified
Animatable
:   No
[CSS Object Model Property](/css/concepts/cssom)
:   ``

## Syntax

-   `float: footnote`
-   `float: left`
-   `float: none`
-   `float: right`

## Values

none
:   `none` indicates that the element does not contain any float at all. This is the initial value of the `float` property.

left
:   The `left` value indicates that the element must float to the far left side of its containing block.

right
:   The `right` value indicates that the element must float to the far right side of its containing block.

footnote
:   The `footnote` value indicates that the element is moved to the footnote area and that a footnote call is put in its original location.

## Examples

In this example, we create a simple layout containing a title, a logo (image) and some textual content. Notice the use of the `clearfix` class on the `article` element below.

``` {.html}
<article class="clearfix">
  <img class="logo" src="http://www.webplatform.org/logo/wplogo_pillow_tan.png" alt="Web Platform Docs logo" />
  <h1>Web Platform Docs</h1>
  <p class="desc">Web Platform Docs is a community-driven site that aims to become a comprehensive and authoritative source for web developer documentation. Learn more about <a href="http://docs.webplatform.org">Web Platform Docs</a>. To understand the <a href="http://docs.webplatform.org/wiki/css/properties/float"><code>float</code></a> and the <a href="https://developer.mozilla.org/en-US/docs/Web/CSS/float#Clearing_floats"><code>clear</code></a> property.</p>
  </div>
</article>
```

[View live example](http://code.webplatform.org/gist/5974883)

The CSS for the above layout is described below. Notice the use of the `float`s.

``` {.css}
/* Some CSS rules remove for brevity; please see the live URL for the complete example. */

.logo {
  float: left;
}

.desc {
  float: left;
  width: 60%;
}
```

[View live example](http://code.webplatform.org/gist/5974883)

## Usage

     As float implicitly implies the use of the block layout, it modifies the computed value of the display values in some cases:

Specified value
:   Computed value
inline
:   block
inline-block
:   block
inline-table
:   table
table-row
:   block
table-row-group
:   block
table-column
:   block
table-column-group
:   block
table-cell
:   block
table-caption
:   block
table-header-group
:   block
table-footer-group
:   block
flex
:   flex, but float has no effect on such elements
inline-flex
:   inline-flex, but float has no effect on such elements
 other
:   unchanged

**Note:** If you're referring to this property from JavaScript as a member of the element.style object, you must spell it as cssFloat. Also note that Internet Explorer versions 8 and older spelled this styleFloat. This is an exception to the rule that the name of the DOM member is the camel-case name of the dash-separated CSS name (and is due to the fact that "float" is a reserved word in JavaScript, as with the need to escape "class" as "className" and escape \<label\>'s "for" as "htmlFor").

## Notes

### Remarks

-   When using floats it's often necessary to clear the parent element. Check out the [clear](/css/properties/clear)-property.
-   Objects following a floating object move in relation to the position of the floating object.
-   The floating object is moved left or right until it reaches the border, padding, or margin of another block-level object.

### Syntax

`float: left | right | none | inherit`

### Standards information

-   [CSS 2.1](http://go.microsoft.com/fwlink/p/?linkid=203757), Section 5.5.25

## Related specifications

Specification
:   Status
[CSS basic box model](http://www.w3.org/TR/css3-box/#floating0)
:   Working Draft
[CSS Level 2 (Revision 1)](http://www.w3.org/TR/CSS2/visuren.html#float-position)
:   Recommendation
[CSS Level 1](http://www.w3.org/TR/CSS1/#float)
:   Recommendation
[CSS Generated Content for Paged Media Module](http://www.w3.org/TR/css3-gcpm/#turning-elements-into-footnotes)
:   Working Draft

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

-   **float**

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

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/CSS/float)

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

