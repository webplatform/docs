---
title: border-left
code_samples:
  - 'http://gist.github.com/5539642'
notes:
  - 'Add specifications and compatibility.'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`For style values, the initial value is none. For color values, the initial value is currentColor.  For width values, the initial value is medium, which is computed as about 3px in most browsers.`'
  'Applies to': 'All elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': '[[Computed value::Depends of the value type, see [\#Computed value](#Computed_value) in [\#Notes](#Notes) for more details]]'
  Animatable: 'Yes'
  '[CSS Object Model Property](/css/concepts/cssom)': '`borderLeft`'
  Percentages: N/A
readiness: 'In Progress'
standardization_status: 'W3C Recommendation'
summary: 'Shorthand property that defines the border-width, border-style and border-color of an element''s left border in a single declaration. Note that you can use the corresponding longhand properties to set specific individual properties of the left border — border-left-width, border-left-style and border-left-color.'
tags:
  - CSS
  - Properties
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/defaultSelected
uri: css/properties/border-left

---
## Summary

Shorthand property that defines the border-width, border-style and border-color of an element's left border in a single declaration. Note that you can use the corresponding longhand properties to set specific individual properties of the left border — border-left-width, border-left-style and border-left-color.

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
:   [[Computed value::Depends of the value type, see [\#Computed value](#Computed_value) in [\#Notes](#Notes) for more details]]

Animatable
:   Yes

[CSS Object Model Property](/css/concepts/cssom)
:   `borderLeft`

Percentages
:   N/A

## Syntax

-   `border-left: border-width border-style color`
-   `border-left: inherit`

## Values

border-width border-style color
:   The `border-left` property can contain up to three components:

-   `border-width`: This takes a numeric value with any of the standard length units.
-   `border-style`: This takes any of the range of style values available to the [**border-style**](/css/properties/border-style) property, which includes `none`, `hidden`, `dotted`, `dashed`, `solid`, `double`, `groove`, `ridge`, `inset`, `outset`. For more details about each, see the [**border-style**](/css/properties/border-style) page.
-   `color`: This can take any valid CSS color as its value.

inherit
:   When we set the value to `inherit`, the element will inherit the border values set on its parent.

## Examples

A simple example showing multiple `<div>`s, identical in style except that they have different `border-left` properties applied to them.

``` html
<div class="one"><p>One</p></div>
<div class="two"><p>Two</p></div>
<div class="three"><p>Three</p></div>
<div class="four"><p>Four</p></div>
<div class="five"><p>Five</p></div>
```

[View live example](http://code.webplatform.org/gist/5539642)

``` css
/**
 * border-left example
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
  /* The most basic border-left example you can show. */
  border-left: 1px solid black;
}

.two {
  /* If you don't explicitly set a color, currentColor is used, which
     equates to the text colour of the element, in this case black.   */
  border-left: 4px dashed;
}

.three {
  /* When no width is specified, the default width medium is used,
     which computes to about 3px in most browsers */
  border-left: dotted red;
}

.four {
  /* When no border style is specified, the border won't appear,
     as the default border style is none. */
  border-left: 10px black;
}

.five {
  /* A more interesting border example to round things off,
     showing a basic border being set, and then the left
     border being overridden */
  border: 1px inset black;
  border-left: 10px inset rgba(234,190,50,0.75);
}
```

[View live example](http://code.webplatform.org/gist/5539642)

## Usage

     * It is usual to use the border-left property to set the default state of a box's left border, and then override individual values using more specific properties, such as border-left-width or border-left-color.

-   `border-left` can be used as a divider between horizontally laid out items, such as horizontal navigation menu items, or table cells.

## Notes

## Computed value

For `style` values, the computed value is as specified. For `width` values, the computed value is the absolute pixel value, or `0` if the value is set to `none` or `hidden`. For `color` values, the computed value is the equivalent RGB value, or the equivalent RGBA value for translucent colors.

## See also

### Related articles

#### Border

-   [border](/css/properties/border)

-   [border-bottom](/css/properties/border-bottom)

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

-   **border-left**

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

### Related pages

-   `CSSStyleDeclaration`
-   `currentStyle`
-   `defaults`
-   `runtimeStyle`
-   `style`
-   `Reference`
-   `border`
-   `Other Resources`
-   `CSS Enhancements in Internet Explorer 6`
