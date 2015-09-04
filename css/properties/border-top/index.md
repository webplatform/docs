---
title: border-top
tags:
  - CSS
  - Properties
readiness: 'In Progress'
standardization_status: 'W3C Recommendation'
notes:
  - 'Add specifications, compatibility.'
summary: 'Shorthand property that defines the border-width, border-style and border-color of an element''s top border in a single declaration. Note that you can use the corresponding longhand properties to set specific individual properties of the top border — border-top-width, border-top-style and border-top-color.'
code_samples:
  - 'http://gist.github.com/5534715'
uri: css/properties/border-top
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/defaultSelected

---
# border-top

## Summary

Shorthand property that defines the border-width, border-style and border-color of an element's top border in a single declaration. Note that you can use the corresponding longhand properties to set specific individual properties of the top border — border-top-width, border-top-style and border-top-color.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `For style values, the initial value is none. For color values, the initial value is currentColor.  For width values, the initial value is medium, which is computed as about 3px in most browsers..`
Applies to
:   All elements
[Inherited](/css/concepts/inherited)
:   No
Media
:   visual
[Computed value](/css/concepts/computed_value)
:   <span class="smwttpersist" data-type="warning" data-context="persitent"><span class="smwtticon warning"></span><span class="smwttcontent">String representation "For \<code\>style … slucent colors." is too long.</span></span>
Animatable
:   Yes
[CSS Object Model Property](/css/concepts/cssom)
:   `borderTop`
Percentages
:   N/A

## Syntax

-   `border-top: border-width border-style color`
-   `border-top: inherit`

## Values

border-width border-style color
:   The `border-top` property can contain up to three components:

-   `border-width`: This takes a numeric value with any of the standard length units.
-   `border-style`: This takes any of the range of style values available to the [**border-style**](/css/properties/border-style) property, which includes `none`, `hidden`, `dotted`, `dashed`, `solid`, `double`, `groove`, `ridge`, `inset`, `outset`. For more details about each, see the [**border-style**](/css/properties/border-style) page.
-   `color`: This can take any valid CSS color as its value.

inherit
:   When we set the value to `inherit`, the element will inherit the border values set on its parent.

## Examples

A simple example showing multiple `<div>`s, identical in style except that they have different `border-top` properties applied to them.

``` {.html}
One
Two
Three
Four
Five
```

[View live example](http://code.webplatform.org/gist/5534715)

``` {.css}
/**
 * border-top example
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
  /* The most basic border-top example you can show. */
  border-top: 1px solid black;
}

.two {
  /* If you don't explicitly set a color, currentColor is used, which
     equates to the text colour of the element, in this case black.   */
  border-top: 4px dashed;
}

.three {
  /* When no width is specified, the default width medium is used,
     which computes to about 3px in most browsers */
  border-top: dotted red;
}

.four {
  /* When no border style is specified, the border won't appear,
     as the default border style is none. */
  border-top: 10px black;
}

.five {
  /* A more interesting border example to round things off,
     showing a basic border being set, and then the right
     border being overridden */
  border: 1px inset black;
  border-top: 10px inset rgba(234,190,50,0.75);
}
```

[View live example](http://code.webplatform.org/gist/5534715)

## Usage

     * It is usual to use the border-top property to set the default state of a box's top border, and then override individual values using more specific propeties, such as border-top-width or border-top-color.

-   `border-top` can be used as a divider between vertically laid out items, such as a vertical navigation menu, or table cells.

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

-   [border-left](/css/properties/border-left)

-   [border-left-color](/css/properties/border-left-color)

-   [border-left-style](/css/properties/border-left-style)

-   [border-left-width](/css/properties/border-left-width)

-   [border-radius](/css/properties/border-radius)

-   [border-right](/css/properties/border-right)

-   [border-right-color](/css/properties/border-right-color)

-   [border-right-style](/css/properties/border-right-style)

-   [border-right-width](/css/properties/border-right-width)

-   **border-top**

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
-   `border`

