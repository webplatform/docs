---
title: custom
tags:
  - Markup
  - Elements
  - HTML
readiness: 'Not Ready'
standardization_status: Non-Standard
notes:
  - "Ancient text from MSDN?\nDeletion Candidate"
summary: 'Represents a user-defined HTML tag (nonstandard)'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/custom.htm'
uri: html/elements/custom

---
# custom

## Summary

Represents a user-defined HTML tag (nonstandard)

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLElement](/dom/HTMLElement)

## Examples

This example uses the **custom** element to create custom RED, GREEN, and BLUE elements. These elements change the color of the text to red, green, or blue, depending on whether it is surrounded by RED, GREEN, or BLUE tags. In this example, the RED, GREEN, and BLUE tags are defined within a namespace called CUSTOMTAG.

    <HTML XMLNS:CUSTOMTAG>
    <HEAD>
    <STYLE>
    @media all {
        CUSTOMTAG\:RED { color: red; }
        CUSTOMTAG\:GREEN { color: green; }
        CUSTOMTAG\:BLUE { color: blue; }
    }
    </STYLE>
    </HEAD>
    <BODY>
    <CUSTOMTAG:RED>
    This text is red because it is enclosed within opening
    and closing CUSTOMTAG:RED tags.
    </CUSTOMTAG:RED>
    <CUSTOMTAG:GREEN>
    This text is green because it is enclosed within opening
    and closing CUSTOMTAG:GREEN tags.
    </CUSTOMTAG:GREEN>
    <CUSTOMTAG:BLUE>
    This text is blue because it is enclosed within opening
    and closing CUSTOMTAG:BLUE tags.
    </CUSTOMTAG:BLUE>
    </BODY>
    </HTML>

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/custom.htm)

## Notes

### Remarks

To declare a namespace, use the [**XMLNS**](/apis/xhr/properties/XMLNS_attribute) attribute of the HTML element. When defining custom tags, you must enclose custom tag definitions within an [**@media**](/css/atrules/@media) wrapper. Custom tags become much more interesting when applied with a Dynamic HTML (DHTML) behavior. Dynamic HTML (DHTML) behaviors (or behaviors) and styles are applied to elements on a page the same way—using Cascading Style Sheets (CSS) attributes. More specifically, the proposed CSS [**behavior**](/css/media_queries/behavior) attribute enables a document author to specify the location of the behavior and apply that behavior to an element. The Windows Internet Explorer support for custom tags on an HTML page requires that a namespace be defined for the tag. Otherwise, the custom tag is treated as an unknown tag when the document is parsed. Although navigating to a page with an unknown tag in Internet Explorer does not result in an error, unknown tags have the disadvantage of not being able to contain other tags, nor can they have behaviors applied to them. This element is available in HTML and script as of Microsoft Internet Explorer 5.

## See also

### Related pages (MSDN)

-   `Using Custom Tags in Internet Explorer`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

