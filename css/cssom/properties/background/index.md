---
title: background
tags:
  - API
  - Object
  - Properties
  - CSS
  - DOM
readiness: 'Ready to Use'
summary: 'The background-position property sets the starting position of a background image.'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/background_h.htm'
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/background_s.htm'
uri: css/cssom/properties/background
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/defaultSelected

---
# background

## Summary

The background-position property sets the starting position of a background image.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration](/css/cssom/CSSStyleDeclaration/CSSStyleDeclaration)</span></span>

## Syntax

``` {.js}
var result = declaration.background;
declaration.background = value;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

## Examples

The following examples use the **background** property and the **background** attribute to set the background values.

This example uses inline event handlers to modify the [**background-color**](/css/properties/background-color) and [**background-position**](/css/properties/background-position) attributes of an image. These attributes are specified in an embedded style sheet using the **background** attribute.

    <STYLE>
    .style1{background:beige url(sphere.jpg) no-repeat top center}
    .style2{background:ivory url(sphere.jpeg) no-repeat bottom right}
    </STYLE>
    </HEAD>
    <BODY>
    <SPAN onmouseover="this.className='style1'"
        onmouseout="this.className='style2'">
    . . .  </SPAN>

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/background_h.htm)

This example uses inline scripting to modify the [**background-color**](/css/properties/background-color) and [**background-position**](/css/properties/background-position) properties of an image.

    <SPAN onclick="this.style.background='beige url(sphere.jpeg)
      no-repeat top center'">
    . . . </SPAN>

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/background_s.htm)

## Notes

### Remarks

The **background** property is a composite property. Separate properties can be used to specify each property, but in many cases it is more convenient to set them in one place using this composite property. Individual background properties not set by the composite background property are set to their default values. For example, the default value for **image** is **none**. Setting **background**: **white** is equivalent to setting **background**: **white** **none** **repeat** **scroll** **0%** **0%**. So, in addition to setting the background color to white, setting **background**: **white** clears any **image**, **repeat**, **attachment**, or **position** values previously set. The background properties render in the object's content and padding; however, borders are set using the [**border**](/css/properties/border) properties. In Microsoft Internet Explorer 3.0, elements that expose the **background** property only support the **color** and **image** values; the **attachment** value is only supported by the **body**, [**table**](/html/elements/table), and **td** elements. In block elements, such as **p** and **div**, background images and colors appear only behind text in Internet Explorer 3.0; in Microsoft Internet Explorer 4.0 and later, backgrounds stretch from margin to margin when used with block elements. Although objects do not inherit the **background** property, the background image or color of an object's parent appears behind an object if a background is not specified. For more information about supported colors, see the Color Table.

### Syntax

`background: '[  <color>  || image || repeat || attachment || position ]`

### Standards information

-   [CSS 2.1](http://go.microsoft.com/fwlink/p/?linkid=203757), Section 5.3.7
-   [Document Object Model (DOM) Level 1 Specification](http://go.microsoft.com/fwlink/p/?linkid=161725), Section 2.5.5

## See also

### Related articles

#### Background

-   **background**

-   [background](/css/properties/background)

-   [background-attachment](/css/properties/background-attachment)

-   [background-blend-mode](/css/properties/background-blend-mode)

-   [background-clip](/css/properties/background-clip)

-   [background-color](/css/properties/background-color)

-   [background-image](/css/properties/background-image)

-   [background-origin](/css/properties/background-origin)

-   [background-position](/css/properties/background-position)

-   [background-position-x](/css/properties/background-position-x)

-   [background-position-y](/css/properties/background-position-y)

-   [background-repeat](/css/properties/background-repeat)

-   [background-size](/css/properties/background-size)

-   [JavaScript animation](/tutorials/animation_in_javascript_2)

### Related pages (MSDN)

-   `CSSStyleDeclaration`
-   `currentStyle`
-   `defaults`
-   `runtimeStyle`
-   `style`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

