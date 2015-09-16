---
title: 'Font related properties'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs more content including examples.'
readiness: 'In Progress'
summary: "Sets font-style, font-variant, font-weight, font-size/line-height, font-family properties in one declaration. \n"
tags:
  - API
  - Objects
  - DOM
uri: css/fonts

---
## Summary

Sets font-style, font-variant, font-weight, font-size/line-height, font-family properties in one declaration.

The order is obligatory, not all options must be set.

*font-size* and *font-family* are required options.

## Properties

*No properties.*

## Methods

*No methods.*

## Events

*No events.*

**Needs Examples**: This section should include examples.

## Usage

     p {
     font: italic 1.2em/1.5 Georgia;
     }

     div {
     font: italic small-caps 1.2em/14px "Times New Roman";
     }

     em { font: bold 1.2em/2ex Arial; }

### In this section

|Property|Description|
|:-------|:----------|
|[**font**](/css/properties/font)|Sets or retrieves a combination of separate [**font**](/css/properties/font) properties of the object. Alternatively, sets or retrieves one or more of six user-preference fonts.Sets or retrieves a combination of separate **font** properties of the object. Alternatively, sets or retrieves one or more of six user-preference fonts.|
|[**font-family**](/css/properties/font-family)|Sets or retrieves the name of the font used for text in the object.|
|[**font-feature-settings**](/css/properties/font-feature-settings)|Gets or sets one or more values that specify glyph substitution and positioning in fonts that include OpenType layout features.|
|[**font-size**](/css/properties/font-size)|Sets or retrieves a value that indicates the font size used for text in the object.|
|[**font-size-adjust**](/css/properties/font-size-adjust)|Sets or retrieves a value that specifies an aspect value for an element that will effectively preserve the x-height of the first choice font, whether it is substituted or not.|
|[**font-stretch**](/css/properties/font-stretch)|Sets or retrieves a value that indicates a normal, condensed, or expanded face of a font family.|
|[**font-style**](/css/properties/font-style)|Sets or retrieves the font style of the object as **italic**, **normal**, or **oblique**.|
|[**font-variant**](/css/fonts/font-variant)|Gets or sets whether the text of the object is in small capital letters.|
|[**font-weight**](/css/properties/font-weight)|Gets of sets the weight of the font of the object.|

## See also

### Related articles

#### Fonts

-   [@font-face](/css/atrules/@font-face)

-   **Font related properties**

-   [font-variant](/css/fonts/font-variant)

-   [font](/css/properties/font)

-   [font-family](/css/properties/font-family)

-   [font-feature-settings](/css/properties/font-feature-settings)

-   [font-kerning](/css/properties/font-kerning)

-   [font-language-override](/css/properties/font-language-override)

-   [font-size](/css/properties/font-size)

-   [font-size-adjust](/css/properties/font-size-adjust)

-   [font-stretch](/css/properties/font-stretch)

-   [font-style](/css/properties/font-style)

-   [font-variant](/css/properties/font-variant)

-   [user-modify](/css/properties/user-modify)

-   [size](/html/attributes/size)

-   [font](/html/elements/font)
