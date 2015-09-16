---
title: clear
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/CSS/clear)'
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
code_samples:
  - 'http://gist.github.com/6042258'
  - 'http://gist.github.com/6065677'
  - 'http://gist.github.com/6065820'
  - 'http://gist.github.com/6065831'
  - 'http://gist.github.com/6072801'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`none`'
  'Applies to': 'Block-level elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'as specified'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`clear`'
  Percentages: N/A
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'The clear CSS property specifies if an element can be positioned next to or must be positioned below the floating elements that precede it in the markup.'
tags:
  - CSS
  - Properties
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/defaultSelected
uri: css/properties/clear

---
## Summary

The clear CSS property specifies if an element can be positioned next to or must be positioned below the floating elements that precede it in the markup.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `none`

Applies to
:   Block-level elements

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   as specified

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:   `clear`

Percentages
:   N/A

## Syntax

-   `clear: both`
-   `clear: inherit`
-   `clear: left`
-   `clear: none`
-   `clear: right`

## Values

none
:   May have adjacent floats on both the left and right sides.

left
:   Floated elements that precede the cleared element are not allowed to the left of the cleared element. The cleared element must move below the floated element.

right
:   Floated elements that precede the cleared element are not allowed to the right of the cleared element. The cleared element must move below the floated element.

both
:   Floated elements that precede the cleared element are not allowed to be adjacent to the cleared element. The cleared element must move below the floated elements.

inherit
:   Takes the same specified value as the property for the element's parent.

## Examples

Example of `clear:none;` in use.

``` css
p{
   /* clear: value; */
   clear: none;
}
```

[View live example](http://code.webplatform.org/gist/6042258)

Example of `clear: left;` in use.

``` css
p{
   /* clear: value; */
   clear: left;
}
```

[View live example](http://code.webplatform.org/gist/6065677)

Example of `clear: right;` in use.

``` css
p{
   /* clear: value; */
   clear: right;
}
```

[View live example](http://code.webplatform.org/gist/6065820)

Example of `clear: both;` in use.

``` css
p{
   /* clear: value; */
   clear: both;
}
```

[View live example](http://code.webplatform.org/gist/6065831)

Moving a footer below all floated content above.

``` html
<h1>Clearing Floats</h1>
<!-- Note that it is a good practice to have your floated items precede the elements they are floated around. -->
<div id="box"><code>float:left</code></div>
<p>Paragraphs are typically <code>clear: none;</code> by default, and are frequently used in conjuction with a floated image. In this example,
pretend the black box labeled <code>float:left;</code> is an image floated left. </p>
<p><a href="javascript:void()" id="toggleClear">Toggle the clear settings on the footer</a></p>
<footer id="footer">This is a footer.</footer>
```

[View live example](http://code.webplatform.org/gist/6072801)

## Notes

The **clear** property applies to both [floating](/css/properties/float) and non-floating elements.
When applied to non-floating blocks, it moves the [border](/css/properties/border) edge of the element down until it is below the margin edge of all relevant floats. This movement (when it happens) causes margin collapsing not to occur.

When applied to floating elements, it moves the margin edge of the element below the margin edge of all relevant floats. This affects the position of later floats, since later floats cannot be positioned higher than earlier ones.

The floats that are relevant to be cleared are the earlier floats within the same block formatting context.

## Related specifications

[CSS Level 2 (Revision 1)](http://www.w3.org/TR/CSS2/visuren.html#propdef-clear)
:   Recommendation

[CSS - Basic Box Model](http://www.w3.org/TR/css3-box/#the-lsquo2)
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

-   **clear**

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

### Other articles

-   [Tutorial: Page layout with floats and clearing](/tutorials/floats_and_clearing).
-   [Tutorial: Exploring the CSS box model](/tutorials/box_model).
-   [Guide: The CSS layout model](/guides/the_css_layout_model).

### Related pages

-   `CSSStyleDeclaration`
-   `currentStyle`
-   `defaults`
-   `runtimeStyle`
-   `style`
