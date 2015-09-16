---
title: -ms-scrollbar-track-color
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Add summery, values, specifications, compatibility.'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: css/properties
    href: /css/properties
standardization_status: Non-Standard
tags:
  - API
  - Object
  - Properties
  - DOM
uri: css/properties/-ms-scrollbar-track-color

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Property of [css/properties](/css/properties)[css/properties](/css/properties)

## Syntax

``` js
var result = element.-ms-scrollbar-track-color;
element.-ms-scrollbar-track-color = value;
```

## Examples

The following example shows how to create a style rule that sets the **-ms-scrollbar-track-color** property for a **textArea** element.

``` html
<HTML>
  <HEAD>
    <STYLE>
      TEXTAREA.BlueTrack  { scrollbar-track-color:blue }
    </STYLE>
  </HEAD>
  <BODY>
    <TEXTAREA CLASS="BlueTrack">The track element in the scroll bar for this
      element will be blue.</TEXTAREA>
  </BODY>
</HTML>
```

## Notes

### Remarks

Windows Internet Explorer 8. The **-ms-scrollbar-track-color** attribute is an extension to CSS, and can be used as a synonym for **scrollbar-track-color** in IE8 Standards mode. The track is the element of a scroll bar on which the scroll box can slide either up and down or left and right. The scroll box is the square box within a scroll bar that can be moved either up and down or left and right on a track to change the position of the content on the screen. This property applies to elements that display a scroll bar. Cascading Style Sheets (CSS) enable scrolling on all objects through the [**overflow**](/css/properties/overflow) property. These objects are not listed in the Applies To list for this property.

### Syntax

`-ms-scrollbar-track-color: variant`

## See also

### Related articles

#### Scrollbar

-   [-ms-scrollbar-3d-light-color](/css/properties/-ms-scrollbar-3d-light-color)

-   [-ms-scrollbar-arrow-color](/css/properties/-ms-scrollbar-arrow-color)

-   [-ms-scrollbar-base-color](/css/properties/-ms-scrollbar-base-color)

-   [-ms-scrollbar-darkshadow-color](/css/properties/-ms-scrollbar-darkshadow-color)

-   [-ms-scrollbar-face-color](/css/properties/-ms-scrollbar-face-color)

-   [-ms-scrollbar-highlight-color](/css/properties/-ms-scrollbar-highlight-color)

-   [-ms-scrollbar-shadow-color](/css/properties/-ms-scrollbar-shadow-color)

-   **-ms-scrollbar-track-color**

### Related pages (MSDN)

-   `CSSStyleDeclaration`
-   `currentStyle`
-   `defaultSelected`
-   `runtimeStyle`
-   `style`
-   `Reference`
-   `-ms-scrollbar-3dlight-color`
-   `-ms-scrollbar-arrow-color`
-   `-ms-scrollbar-base-color`
-   `-ms-scrollbar-darkshadow-color`
-   `-ms-scrollbar-face-color`
-   `-ms-scrollbar-highlight-color`
-   `-ms-scrollbar-shadow-color`
