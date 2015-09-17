---
title: '-ms-scrollbar-highlight-color'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://result.webplatform.org/gist/7331495'
notes:
  - 'Add summery, values, specifications, compatibility.'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: css/properties/-ms-scrollbar-highlight-color
standardization_status: Non-Standard
tags:
  - API_Object_Properties
  - DOM
  - Needs_Summary
uri: css/properties/-ms-scrollbar-highlight-color

---
Property of **css/properties/-ms-scrollbar-highlight-colorcss/properties/-ms-scrollbar-highlight-color**

## Syntax

``` js
var result = -ms-scrollbar-highlight-color.-ms-scrollbar-highlight-color;
-ms-scrollbar-highlight-color.-ms-scrollbar-highlight-color = scrollbar-highlight-color:blue;
```

## Examples

The following example shows how to create a style rule that sets the **-ms-scrollbar-highlight-color** property.

``` html
<html>
  <head>
    <style>
        textarea  { scrollbar-highlight-color:blue }
    </style>
  </head>
  <body>
    <textarea>The scroll bar face for this element will turn blue when a scroll bar button is pressed.
  </textarea>
  </body>
</html>
```

[View live example](http://result.webplatform.org/gist/7331495)

## Usage

     -ms-scrollbar-highlight-color: purple

## Notes

### Remarks

This property is specific to Internet Explorer 8. The **-ms-scrollbar-highlight-color** attribute is an extension to CSS, and can be used as a synonym for **scrollbar-highlight-color** in IE8 Standards mode.

The scroll box is the square box within a scroll bar that can be moved either up and down or left and right on a track to change the position of the content on the screen. The scroll arrows, located at each end of a scroll bar, are the square buttons containing the arrows that move the content on the screen in small increments, either up and down or left and right.

This property applies to elements that display a scroll bar. Cascading Style Sheets (CSS) enable scrolling on all objects through the [**overflow**](/css/properties/overflow) property. These objects are not listed in the Applies To list for this property.

### Standards information

There are no standards that apply here.

## See also

### Related articles

#### Scrollbar

-   [-ms-scrollbar-3d-light-color](/css/properties/-ms-scrollbar-3d-light-color)

-   [-ms-scrollbar-arrow-color](/css/properties/-ms-scrollbar-arrow-color)

-   [-ms-scrollbar-base-color](/css/properties/-ms-scrollbar-base-color)

-   [-ms-scrollbar-darkshadow-color](/css/properties/-ms-scrollbar-darkshadow-color)

-   [-ms-scrollbar-face-color](/css/properties/-ms-scrollbar-face-color)

-   **-ms-scrollbar-highlight-color**

-   [-ms-scrollbar-shadow-color](/css/properties/-ms-scrollbar-shadow-color)

-   [-ms-scrollbar-track-color](/css/properties/-ms-scrollbar-track-color)

### Related pages

-   CSSStyleDeclaration[CSSStyleDeclaration](/css/cssom/CSSStyleDeclaration/CSSStyleDeclaration)
-   currentStyle[currentStyle](/css/cssom/currentStyle)
-   defaultSelected[defaultSelected](/dom/HTMLOptionElement/defaultSelected)
-   runtimeStyle[runtimeStyle](/css/cssom/runtimeStyle)
-   style[style](/css/cssom/style)
-   `Reference`
-   -ms-scrollbar-3dlight-color[-ms-scrollbar-3dlight-color](/css/properties/-ms-scrollbar-3d-light-color)
-   -ms-scrollbar-arrow-color[-ms-scrollbar-arrow-color](/css/properties/-ms-scrollbar-arrow-color)
-   -ms-scrollbar-base-color[-ms-scrollbar-base-color](/css/properties/-ms-scrollbar-base-color)
-   -ms-scrollbar-darkshadow-color[-ms-scrollbar-darkshadow-color](/css/properties/-ms-scrollbar-darkshadow-color)
-   -ms-scrollbar-face-color[-ms-scrollbar-face-color](/css/properties/-ms-scrollbar-face-color)
-   -ms-scrollbar-shadow-color[-ms-scrollbar-shadow-color](/css/properties/-ms-scrollbar-shadow-color)
-   -ms-scrollbar-track-color[-ms-scrollbar-track-color](/css/properties/-ms-scrollbar-track-color)
