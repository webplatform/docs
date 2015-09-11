---
title: background-position-x
attributions:
  - 'Microsoft Developer Network: [[[1]](http://msdn.microsoft.com/en-us/library/ff521123(v=vs.85).aspx) Article]'
notes:
  - "Add specifications, compatibility.\nSupported by IE, Safari, and Chrome. But not appear in the Spec."
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`0%`'
  'Applies to': 'All elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'as specified'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
readiness: 'In Progress'
standardization_status: Non-Standard
summary: 'Sets the horizontal position of a background image.'
tags:
  - CSS
  - Properties
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/defaultSelected
uri: css/properties/background-position-x

---
## <span>Summary</span>

Sets the horizontal position of a background image.

## <span>Overview table</span>

[Initial value](/css/concepts/initial_value)
:   `0%`

Applies to
:   All elements

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   as specified

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:

## <span>Syntax</span>

-   `background-position-x: hAlignment`
-   `background-position-x: length`
-   `background-position-x: percentage`

## <span>Values</span>

length
:   Floating-point number, followed by an absolute units designator (`cm`, `mm`, `in`, `pt`, or `pc`) or a relative units designator (`em`, `ex`, or `px`). For more information about the supported length units, see CSS Values and Units Reference.

percentage
:   Integer, followed by a percent sign (%). The value is a percentage of the width or height of the object.

hAlignment
:   Horizontal alignment value (e.g. "left", "right", or "center").

## <span>Examples</span>

Moving the background image to the right by 50px.

``` css
background-position-x: 50px;
```

Moving the background image to the left by 50px.

``` css
background-position-x: -50px;
```

Moving the background image to the right by half the width of its element.

``` css
background-position-x: 50%;
```

Moving the background image to the left by half the width of its element.

``` css
background-position-x: -50%;
```

Centering a background image inside its element.

``` css
background-position-x: center;
```

## <span>Usage</span>

     ===Usage===

-   Often used to manipulate sprites (i.e. a technique of using CSS to expose small portions of a single background image, which is composed of multiple smaller images, such that HTTP requests are reduced).
-   If browser support is of utmost importance, use [background-position](http://docs.webplatform.org/wiki/css/properties/background-position) instead.

## <span>Notes</span>

### <span>Remarks</span>

-   Windows Internet Explorer 8. The **-ms-background-position-x** attribute is an extension to CSS, and can be used as a synonym for **background-position-x** in IE8 Standards mode.

-   Although background-position-x is currently non-standard, Jonathan Snook provides a case for its inclusion regarding right-to-left languages, such as Arabic or Hebrew. When using sprites, developers would be able to accomodate LTR and RTL environments with a single line of code by including the background-position-x property, rather than redeclaring every single sprite's position in their stylesheet. [Read his blog entry on this and the background-position-y property.](http://snook.ca/archives/html_and_css/background-position-x-y)

### <span>Syntax</span>

`background-position-x: length | percentage | hAlignment`

### <span>Standards information</span>

There are no standards that apply here.

## <span>Related specifications</span>

[ ]
:

## <span>See also</span>

### <span>Related articles</span>

#### <span>Background</span>

-   [background](/css/cssom/properties/background)

-   [background](/css/properties/background)

-   [background-attachment](/css/properties/background-attachment)

-   [background-blend-mode](/css/properties/background-blend-mode)

-   [background-clip](/css/properties/background-clip)

-   [background-color](/css/properties/background-color)

-   [background-image](/css/properties/background-image)

-   [background-origin](/css/properties/background-origin)

-   [background-position](/css/properties/background-position)

-   **background-position-x**

-   [background-position-y](/css/properties/background-position-y)

-   [background-repeat](/css/properties/background-repeat)

-   [background-size](/css/properties/background-size)

-   [JavaScript animation](/tutorials/animation_in_javascript_2)

### <span>Related pages</span>

-   `CSSStyleDeclaration`
-   `currentStyle`
-   `defaults`
-   `runtimeStyle`
-   `style`
-   `background-position-y`
