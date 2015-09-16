---
title: 'accelerator'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Add summery, values, specifications, compatibility.'
readiness: 'In Progress'
tags:
  - API
  - Objects
  - DOM
uri: 'css/media queries/accelerator'

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

## Properties

*No properties.*

## Methods

*No methods.*

## Events

*No events.*

## Examples

This example uses the **-ms-accelerator** attribute in a **u** element to specify that the `N` in the **label** element is a keyboard shortcut. When the option to "Hide keyboard navigation indicators until I use the Alt key" is enabled in the user's Display Properties, the `N` is not underlined until the user presses the ALT key. When ALT+N is pressed, the **input** element that defines an [**accessKey**](/html/attributes/accessKey) attribute value of 'N' receives the focus.

``` html
<LABEL FOR="oName"><U STYLE="ACCELERATOR:true">N</U>ame: </LABEL>
<INPUT TYPE="text"
    ID="oName"
    SIZE="25"
    ACCESSKEY="N"
    VALUE="Your name here">
```

## Notes

### Remarks

This property is supported by Windows 2000 and later, which enables users to hide navigation indicators for menu items and controls until the ALT key is pressed. An access key is a single character used as a keyboard shortcut for selecting an object. Press and hold the ALT key followed by the character to move input focus and invoke the default event associated with an object. Windows Internet Explorer 8. The **-ms-accelerator** attribute is an extension to CSS, and can be used as a synonym for **accelerator** in IE8 Standards mode.

### Syntax

`-ms-accelerator: false | true`

## See also

### Related articles

#### Media Queries

-   [Responsive Web Design](/concepts/mobile_web/responsive_design)

-   [\<resolution\>](/css/data_types/resolution)

-   **accelerator**

-   [MediaQueryList](/css/media_queries/apis/MediaQueryList)

-   [MediaQueryListListener](/css/media_queries/apis/MediaQueryListListener)

-   [StyleMedia](/css/media_queries/apis/StyleMedia)

-   [addListener](/css/media_queries/apis/addListener)

-   [handleChange](/css/media_queries/apis/handleChange)

-   [matchMedia](/css/media_queries/apis/matchMedia)

-   [matchMedium](/css/media_queries/apis/matchMedium)

-   [matches](/css/media_queries/apis/matches)

-   [media](/css/media_queries/apis/media)

-   [type](/css/media_queries/apis/properties/type)

-   [removeListener](/css/media_queries/apis/removeListener)

-   [Colors by](/css/media_queries/colors_by)

-   [device-height](/css/media_queries/device-height)

-   [filter](/css/media_queries/filter)

-   [ms-interpolation-mode](/css/media_queries/ms-interpolation-mode)

-   [behavior](/css/properties/behavior)

### Related pages

-   CSSStyleDeclaration[CSSStyleDeclaration](/css/cssom/CSSStyleDeclaration/CSSStyleDeclaration)
-   currentStyle[currentStyle](/css/cssom/currentStyle)
-   defaultSelected[defaultSelected](/dom/HTMLOptionElement/defaultSelected)
-   runtimeStyle[runtimeStyle](/css/cssom/runtimeStyle)
-   style[style](/css/cssom/style)
-   accessKey[accessKey](/html/attributes/accessKey)
