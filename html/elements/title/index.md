---
title: title
tags:
  - Markup
  - Elements
  - HTML
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Defines the title of the current document.'
uri: html/elements/title

---
# title

## Summary

Defines the title of the current document.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLTitleElement](/dom/HTMLTitleElement)

## Examples

This example uses the **title** element to specify a title for the document.

``` {.html}
<!doctype html>
<html>
<head>
<title>WebPlatform.org - Your Web, documented</title>
</head>
</html>
```

This example uses the **title** element to provide the current page title as well as the category and the title of the website.

``` {.html}
<!doctype html>
<html>
<head>
<title>title • html • WebPlatform.org</title>
</head>
</html>
```

## Usage

     You can only have one title element per page. The content of this element should make sense out of context, and is commonly used in the browser title bar, and labels for favorites/bookmarks. It is usually also displayed as a title on search engine results pages.

The title element varies from the [h1](/html/elements/hn) element in that the heading elements can be contextual: they do not need to make sense out-of-context.

It is read by screen readers as soon as the web page has finished loading and is the first information assistive technologies receive. It can be used to convey information immediately to users using such tools, like the success or error of a form submission.

Titles of sub pages should provide the most specific information on front (“front-loading”), for example a website might first provide the title of the current page, then the name of the category and the name of the complete website.

## Notes

It can only contain text and any contained tags are not interpreted.

There are rare cases where the title is allowed to be omitted. This is the case when a higher-level protocol provides title information, like the subject line of an e-mail.

## Related specifications

Specification
:   Status
[HTML 5.1](http://www.w3.org/TR/html51/document-metadata.html#the-title-element)
:   W3C Working Draft
[HTML 5](http://www.w3.org/TR/html5/document-metadata.html#the-title-element)
:   W3C Recommendation
[HTML 4.01](http://www.w3.org/TR/html401/struct/global.html#edef-TITLE)
:   W3C Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

