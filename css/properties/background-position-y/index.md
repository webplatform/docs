---
title: background-position-y
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - "Add example, description, compatibility.\nSupported by IE, Safari, and Chrome. But not appear in the Spec."
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`0%`'
  'Applies to': 'All elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': ''
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
  Percentages: 'Width or height of the element'
readiness: 'In Progress'
standardization_status: Non-Standard
summary: 'Sets vertical starting position of a background image.'
tags:
  - CSS
  - Properties
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/defaultSelected
uri: css/properties/background-position-y

---
## Summary

Sets vertical starting position of a background image.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `0%`

Applies to
:   All elements

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

Percentages
:   Width or height of the element

## Syntax

-   `background-position-y: length`
-   `background-position-y: percentage`
-   `background-position-y: vAlignment`

## Values

length
:   Floating-point number, followed by an absolute units designator (`cm`, `mm`, `in`, `pt`, or `pc`) or a relative units designator (`em`, `ex`, or `px`). For more information about the supported length units, see CSS Values and Units Reference.

percentage
:   Integer, followed by a percent sign (%). The value is a percentage of the width or height of the object.

vAlignment
:   Vertical alignment value.

**Needs Examples**: This section should include examples.

## Notes

### Remarks

Windows Internet Explorer 8. The **-ms-background-position-y** attribute is an extension to CSS, and can be used as a synonym for **background-position-y** in IE8 Standards mode.

### Syntax

`-ms-background-position-y: length | percentage | vAlignment`

### Standards information

There are no standards that apply here.

## See also

### Related articles

#### Background

-   [background](/css/cssom/properties/background)

-   [background](/css/properties/background)

-   [background-attachment](/css/properties/background-attachment)

-   [background-blend-mode](/css/properties/background-blend-mode)

-   [background-clip](/css/properties/background-clip)

-   [background-color](/css/properties/background-color)

-   [background-image](/css/properties/background-image)

-   [background-origin](/css/properties/background-origin)

-   [background-position](/css/properties/background-position)

-   [background-position-x](/css/properties/background-position-x)

-   **background-position-y**

-   [background-repeat](/css/properties/background-repeat)

-   [background-size](/css/properties/background-size)

-   [JavaScript animation](/tutorials/animation_in_javascript_2)

### Related pages (MSDN)

-   `CSSStyleDeclaration`
-   `currentStyle`
-   `defaults`
-   `runtimeStyle`
-   `style`
-   `-ms-background-position-x`
