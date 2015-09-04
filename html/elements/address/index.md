---
title: address
tags:
  - Markup
  - Elements
  - HTML
readiness: 'Not Ready'
notes:
  - 'Add syntax, attribute, example, compatibility.'
summary: 'The address element (<address>) encloses contact information of the owner or the author of the document or the article.'
uri: html/elements/address

---
# address

## Summary

The address element (\<address\>) encloses contact information of the owner or the author of the document or the article.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLElement](/dom/HTMLElement)

-   The address element must not be used to represent arbitrary addresses, unless those addresses are in fact the relevant contact information.
-   The address element must not contain information other than contact information.
-   Typically, the address element would be included along with other information in a footer element.

## Examples

A page at the W3C Web site might include the following contact information

    <address>
        <p><a href="http://www.w3.org/Consortium/contact-mit">MIT</a></p>
    </address>

Example of information that would be incorrect if placed inside an address element

    <div>Last Modified: 1999/12/24 23:37:50</div>

## Notes

Webkit (Safari, old Android and similar) and Trident (Internet Explorer) user agent default style -

    address {
        display:block;
        font-style: italic;
    }

Gecko (Firefox) user agent default style -

    address, address[dir]{
             unicode-bidi: -moz-isolate;
             display:block;
             font-style:italic;
    }

### Standards information

-   [HTML 4.01 Specification](http://go.microsoft.com/fwlink/p/?linkid=25320), Section 7.5.6

### HTML information

Closing Tag
:   required
CSS Display
:   block

Â

## Related specifications

Specification
:   Status
[HTML 5.1](http://www.w3.org/TR/html51/sections.html#the-address-element)
:   W3C Working Draft
[HTML 5](http://www.w3.org/TR/html5/sections.html#the-address-element)
:   W3C Recommendation
[HTML 4.01](http://www.w3.org/TR/html401/struct/global.html#edef-ADDRESS)
:   W3C Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

