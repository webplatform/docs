---
title: 'box-direction'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: box-direction
  topic: css
notes:
  - 'Add summery, example, compatibility.'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`normal`'
  'Applies to': 'box elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': ''
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
readiness: 'In Progress'
standardization_status: Non-Standard
summary: Deprecated
tags:
  - CSS
  - Properties
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - '-ms-flex-direction'
    - '-ms-box-orient'
uri: css/properties/box-direction

---
## Summary

Deprecated

## Overview table

[Initial value](/css/concepts/initial_value)
:   `normal`

Applies to
:   box elements

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:

## Syntax

-   `box-direction: inherit`
-   `box-direction: normal`
-   `box-direction: reverse`

## Values

normal
:   Default.

Child elements are displayed in the same order that they are declared in the source document.

If the parent element has a computed value for [**-ms-box-orient**](/css/properties/ms-box-orient) of `horizontal`, the child elements are displayed from left to right.

If the parent element has a computed value for [**-ms-box-orient**](/css/properties/ms-box-orient) of `vertical`, the child elements are displayed from top to bottom.

reverse
:   Child elements are displayed in the reverse order that they are declared in the source document.

If the parent element has a computed value for [**-ms-box-orient**](/css/properties/ms-box-orient) of `horizontal`, the child elements are displayed from right to left.

If the parent element has a computed value for [**-ms-box-orient**](/css/properties/ms-box-orient) of `vertical`, the child elements are displayed from bottom to top.

inherit
:   Child elements are displayed in the same order as the computed value of this property for the parent element.

**Needs Examples**: This section should include examples.

## Usage

     Do not use. This property has been replaced by the -ms-flex-direction property, and is no longer recognized by Windows Internet Explorer. To ensure compatibility in the future, applications using this property should be updated accordingly. Gets or sets a value that specifies the display order (along the axis defined by the -ms-box-orient property) of all child elements of the object.

This property is read/write.

### Syntax

`-ms-box-direction: normal | reverse | inherit`

### Standards information

-   [Flexible Box Layout Module](http://go.microsoft.com/fwlink/p/?linkid=223142), Section 3

## Related specifications

[Flexible Box Layout Module](http://www.w3.org/TR/2009/WD-css3-flexbox-20090723/)
:   W3C Working Draft (Obsolete)

## See also

### Related pages

-   CSSStyleDeclaration[CSSStyleDeclaration](/css/cssom/CSSStyleDeclaration/CSSStyleDeclaration)
-   currentStyle[currentStyle](/css/cssom/currentStyle)
-   style[style](/css/cssom/style)
