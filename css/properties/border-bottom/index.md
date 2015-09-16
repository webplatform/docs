---
title: border-bottom
code_samples:
  0: 'http://gist.github.com/5539585'
  2: 'http://gist.github.com/5704867'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`For style values, the initial value is none. For color values, the initial value is currentColor.  For width values, the initial value is medium, which is computed as about 3px in most browsers.`'
  'Applies to': 'All elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'See **Notes** below.'
  Animatable: 'Yes'
  '[CSS Object Model Property](/css/concepts/cssom)': '`borderBottom`'
  Percentages: N/A
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Shorthand property that defines the border-width, border-style and border-color of an element''s bottom border in a single declaration. Note that you can use the corresponding longhand properties to set specific individual properties of the bottom border — border-bottom-width, border-bottom-style and border-bottom-color.'
tags:
  - CSS
  - Properties
uri: css/properties/border-bottom

---
## Summary

Shorthand property that defines the border-width, border-style and border-color of an element's bottom border in a single declaration. Note that you can use the corresponding longhand properties to set specific individual properties of the bottom border — border-bottom-width, border-bottom-style and border-bottom-color.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `For style values, the initial value is none. For color values, the initial value is currentColor.  For width values, the initial value is medium, which is computed as about 3px in most browsers.`

Applies to
:   All elements

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   See **Notes** below.

Animatable
:   Yes

[CSS Object Model Property](/css/concepts/cssom)
:   `borderBottom`

Percentages
:   N/A

## Syntax

-   `border-bottom: border-width border-style color`
-   `border-bottom: inherit`

## Values

border-width border-style color
:   The `border-bottom` property can contain up to three components:

-   `border-width`: This takes a numeric value with any of the standard length units.
-   `border-style`: This takes any of the range of style values available to the [**border-style**](/css/properties/border-style) property, which includes `none`, `hidden`, `dotted`, `dashed`, `solid`, `double`, `groove`, `ridge`, `inset`, `outset`. For more details about each, see the [**border-style**](/css/properties/border-style) page.
-   `color`: This can take any valid CSS color as its value.

inherit
:   When we set the value to `inherit`, the element will inherit the border values set on its parent.

## Examples

``` css
/**
 * border-bottom example
**/

div {
  width: 150px;
  height: 50px;
  margin: 1rem;
  float: left;
}

p {
  padding: 0.25rem;
}

.one {
  /* The most basic border-bottom example you can show. */
  border-bottom: 1px solid black;
}

.two {
  /* If you don't explicitly set a color, currentColor is used, which
     equates to the text colour of the element, in this case black.   */
  border-bottom: 4px dashed;
}

.three {
  /* When no width is specified, the default width medium is used,
     which computes to about 3px in most browsers */
  border-bottom: dotted red;
}

.four {
  /* When no border style is specified, the border won't appear,
     as the default border style is none. */
  border-bottom: 10px black;
}

.five {
  /* A more interesting border example to round things off,
     showing a basic border being set, and then the bottom
     border being overridden */
  border: 1px inset black;
  border-bottom: 10px inset rgba(234,190,50,0.75);
}
```

[View live example](http://code.webplatform.org/gist/5539585)

A simple example showing multiple `<div>`s, identical in style except that they have different `border-bottom` properties applied to them.

``` html
<div class="one"><p>One</p></div>
<div class="two"><p>Two</p></div>
<div class="three"><p>Three</p></div>
<div class="four"><p>Four</p></div>
<div class="five"><p>Five</p></div>
```

[View live example](http://code.webplatform.org/gist/5539585)

An example showing the use of border-bottom property with the hover effect...It gives a beautiful result

``` css
/**
 * Example of border-bottom property

 */

#withoutBullets ul {
    color: #f06;
    font: italic 100% Georgia, serif;
    width: 500px;
    padding:10px;
    margin:10px;
    list-style-type:none;   /*To remove the default bullet style*/
}
#withoutBullets li{
    display:inline;
    margin:8px;
    padding:4px;
}
#withoutBullets li:hover{
    border-bottom:3px solid black;
    border-radius:4px;
}
a:link{text-decoration:none;color:green;}
a:hover{text-decoration:none;color:green;}
a:active{text-decoration:none;color:green;}
a:visited{text-decoration:none;color:green;}
```

[View live example](http://code.webplatform.org/gist/5704867)

## Usage

     * It is usual to use the border-bottom property to set the default state of a box's bottom border, and then override individual values using more specific propeties, such as border-bottom-width or border-bottom-color.

-   `border-bottom` can be used as a divider between vertically laid out items, such as a vertical navigation menu, or table cells.

## Notes

### Computed values

For `style` values, the computed value is as specified. For `width` values, the computed value is the absolute pixel value, or `0` if the value is set to `none` or `hidden`. For `color` values, the computed value is the equivalent RGB value, or the equivalent RGBA value for translucent colors.

## Related specifications

[CSS Level 3](http://www.w3.org/TR/css3-background/#borders)
:   Candidate Recommendation

[CSS Level 2 (Revision 1)](http://www.w3.org/TR/CSS2/box.html#border-shorthand-properties)
:   Recommendation

[CSS Level 1](http://www.w3.org/TR/CSS1/#border)
:   Recommendation

## See also

### Related articles

#### Border

-   [border](/css/properties/border)

-   **border-bottom**

-   [border-bottom-color](/css/properties/border-bottom-color)

-   [border-bottom-left-radius](/css/properties/border-bottom-left-radius)

-   [border-bottom-style](/css/properties/border-bottom-style)

-   [border-bottom-width](/css/properties/border-bottom-width)

-   [border-color](/css/properties/border-color)

-   [border-image](/css/properties/border-image)

-   [border-image-outset](/css/properties/border-image-outset)

-   [border-image-repeat](/css/properties/border-image-repeat)

-   [border-image-slice](/css/properties/border-image-slice)

-   [border-image-source](/css/properties/border-image-source)

-   [border-image-width](/css/properties/border-image-width)

-   [border-left](/css/properties/border-left)

-   [border-left-color](/css/properties/border-left-color)

-   [border-left-style](/css/properties/border-left-style)

-   [border-left-width](/css/properties/border-left-width)

-   [border-radius](/css/properties/border-radius)

-   [border-right](/css/properties/border-right)

-   [border-right-color](/css/properties/border-right-color)

-   [border-right-style](/css/properties/border-right-style)

-   [border-right-width](/css/properties/border-right-width)

-   [border-top](/css/properties/border-top)

-   [border-top-color](/css/properties/border-top-color)

-   [border-top-left-radius](/css/properties/border-top-left-radius)

-   [border-top-right-radius](/css/properties/border-top-right-radius)

-   [border-top-style](/css/properties/border-top-style)

-   [border-top-width](/css/properties/border-top-width)

-   [border-width](/css/properties/border-width)

### Related pages (MSDN)

-   `CSSStyleDeclaration`
-   `currentStyle`
-   `defaultsSelected`
-   `runtimeStyle`
-   `style`
-   `Reference`
-   `border`
-   `Other Resources`
-   `CSS Enhancements in Internet Explorer 6`
