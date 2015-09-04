---
title: link
tags:
  - Markup
  - Elements
  - HTML
readiness: 'Almost Ready'
standardization_status: 'W3C Recommendation'
notes:
  - 'Discussion on semantics of hyperlinks'
summary: 'Enables the current document to establish links to external documents.'
uri: html/elements/link

---
# link

## Summary

Enables the current document to establish links to external documents.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLLinkElement](/dom/HTMLLinkElement)

The \<link\> element allows authors to link their document to other resources. It carries the same semantics as any hyperlink, or the HTTP `Link:` header.

## Attributes

-   `href` = URL potentially surrounded by spaces
    Specifies a URL that provides the destination of the link.
-   `rel` = set of space-separated tokens
    Specifies a list of tokens that specify the relationship between the document containing the link and the destination indicated by the link.Two categories of links can be created using the link element: Links to external resources and hyperlinks:
-   `media` = media-query list
    The media for which the destination of the hyperlink was designed.
    If the link is a hyperlink then the media attribute is purely advisory, and describes for which media the document in question was designed.
    However, if the link is an external resource link, then the media attribute is prescriptive. The user agent must apply the external resource when the media attribute's value matches the environment and the other relevant conditions apply, and must not apply it otherwise.
    The default, if the media attribute is omitted, is "all", meaning that by default links apply to all media.
-   `hreflang` = language tag
    The language of the destination of the hyperlink.
    A valid language tag, as defined in [BCP47].
-   `type` = A valid MIME type that destination of the hyperlink.
    gives the MIME type of the linked resource.
    The default value for the type attribute, which is used if the attribute is absent, is "text/css".
-   `sizes` = icon sizes
    The sizes attribute is used with the icon link type. The attribute must not be specified on link elements that do not have a rel attribute that specifies the icon keyword.
-   Also, the title attribute has special semantics on this element. The exception is for style sheet links, where the title attribute defines alternative style sheet sets.

## Link relations

A URI or any IANA Link can be used as the link `rel=""`, but HTML defines special semantics for many of them:

Link type
:   Category
alternate
:   Hyperlink
archives
:   Hyperlink
author
:   Hyperlink
first
:   Hyperlink
help
:   Hyperlink
icon
:   External Resource
index
:   Hyperlink
last
:   Hyperlink
license
:   Hyperlink
next
:   Hyperlink
pingback
:   External Resource
prefetch
:   External Resource
prev
:   Hyperlink
search
:   Hyperlink
stylesheet
:   External Resource
sidebar
:   Hyperlink
tag
:   Hyperlink
up
:   Hyperlink

## Examples

This example uses the **link** element to apply an external style sheet, called styles.css, to the page.

``` {.html}
<link rel=stylesheet href="styles.css" type="text/css"/>
```

## Notes

### Remarks

The **link** element can be used only within the **head** tag. Windows Internet Explorer 8 and later. The behavior of the [**href**](/html/attributes/href) and the [**rel**](/html/attributes/rel) attributes depends on the current document compatibility mode.

### IANA Link Relations database

The IANA maintains a registry of valid link relations at their [Link Relations registry](http://www.iana.org/assignments/link-relations/link-relations.xhtml), established in [RFC5988](https://tools.ietf.org/html/rfc5988).

## Related specifications

Specification
:   Status
[HTML 5.1](http://www.w3.org/TR/html51/document-metadata.html#the-link-element)
:   W3C Working Draft
[HTML 5](http://www.w3.org/TR/html5/document-metadata.html#the-link-element)
:   W3C Recommendation
[HTML 4.01](http://www.w3.org/TR/html401/struct/links.html#edef-LINK)
:   W3C Recommendation
[RFC 5988: Web Linking](https://tools.ietf.org/html/rfc5988)
:   Standards Track
[Subresource Integrity](http://www.w3.org/TR/SRI/)
:   W3C Working Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

