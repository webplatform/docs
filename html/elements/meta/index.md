---
title: 'meta'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: meta
  topic: html
notes:
  - "Format HTML attributes list\nUser agent support per property"
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLMetaElement](/dom/HTMLMetaElement)'
readiness: 'Not Ready'
standardization_status: 'W3C Recommendation'
summary: 'The &lt;meta&gt; element embeds various kinds of metadata that cannot be expressed using the title, base, link, style, and script elements.'
tags:
  - Markup
  - Elements
  - HTML
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/methods/setAttribute
uri: html/elements/meta

---
## Summary

The &lt;meta&gt; element embeds various kinds of metadata that cannot be expressed using the title, base, link, style, and script elements.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLMetaElement](/dom/HTMLMetaElement)

## Attributes

-   `name` = string
    Sets document metadata.
    -   application-name
        Giving the name of the Web application that the page represents.
    -   author
        Giving the name of one of the page's authors.
    -   description
        Describes the page. [[Example A]](#Example_A)
    -   generator
        Identifies one of the software packages used to generate the document.
    -   keywords
        Giving the keyword relevant to the page. [[Example A]](#Example_A)

Other metadata names may be registered in the WHATWG Wiki MetaExtensions page.

-   `http-equiv` = string
    When the http-equiv attribute is specified on a meta element, the element is a pragma directive.
    -   content-language
        Sets the pragma-set default language.
    -   content-type
        Alternative form of setting the charset attribute
    -   default-style
        Sets the name of the default alternative style sheet set.
    -   refresh
        Acts as timed redirect. [[Example B]](#Example_B)

-   `content` = string
    Gives the value of the document metadata or pragma directive when the element is used for those purposes.

-   `charset` = character encoding name
    Specifies the character encoding used by the document. [[Example A]](#Example_A)

## Internationalization

-   [Declaring the character encoding for HTML](http://www.w3.org/International/techniques/authoring-html#indoc)
-   [Choosing and applying a character encoding](http://www.w3.org/International/techniques/authoring-html#choosing)
-   [Changing to UTF-8](http://www.w3.org/International/techniques/authoring-html#changing)

## Examples

A minimal HTML document with meta information.

``` html
<html>
<head>
  <title>World Wide Web Consortium (W3C)</title>
  <meta charset=utf-8" />
  <meta name="description"
        content="The World Wide Web Consortium (W3C) is an international community
        where Member organizations, a full-time staff,
        and the public work together to develop Web standards." />
  <meta name="keyword" content="W3C, HTML, CSS, SVG, Web standards" />
</head>
<body></body>
</html>
```

## Notes

### Remarks

The **META** element also embeds document information that some search engines use to index and categorize documents on the World Wide Web. This element can be used only within the **HEAD** element. Windows Internet Explorer 8 or later. The behavior of the [**setAttribute**](/w/index.php?title=dom/methods/setAttribute&action=edit&redlink=1) method depends on the current document compatibility mode. For more information, see Attribute Differences in Internet Explorer 8

## Related specifications

[HTML 5.1](http://www.w3.org/TR/html51/document-metadata.html#the-meta-element)
:   W3C Working Draft

[HTML 5](http://www.w3.org/TR/html5/document-metadata.html#the-meta-element)
:   W3C Recommendation

[HTML 4.01](http://www.w3.org/TR/html401/struct/global.html#edef-META)
:   W3C Recommendation

## See also

### Related pages

-   `Reference`
-   `content`
-   httpEquiv[httpEquiv](/html/attributes/httpEquiv)
-   `Conceptual`
-   `Defining Document Compatibility`
