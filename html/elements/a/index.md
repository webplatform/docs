---
title: a
tags:
  - Markup
  - Elements
  - HTML
readiness: 'In Progress'
standardization_status: 'W3C Recommendation'
notes:
  - 'Add more example'
summary: 'Defines a hyperlink, a destination of hyperlink, or both.'
code_samples:
  - 'http://gist.github.com/5281100'
uri: html/elements/a

---
# a

## Summary

Defines a hyperlink, a destination of hyperlink, or both.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLAnchorElement](/dom/HTMLAnchorElement)

### Description

The `a` element defines a hyperlink to any content, which could be an external site, another page on the same site, a section within the same page, an image, or a local file.

### Syntax

    <a href="[URI]">[Anchor text or image tag]</a>

    <a id="#[identifier]">[Anchor text or image tag]</a>

    <a>[Anchor text or image tag]</a>

### Enclosed HTML

HTML enclosed by the `<a></a>` tags is typically text or an image. It is displayed in the page and (if the [href](/html/attributes/href) attribute is present) is rendered as a link.

### Common Attributes

Name
:   Value
[**download**](/html/attributes/download)
:   text
[**href**](/html/attributes/href)
:   [URI](http://www.w3.org/Addressing/URL/uri-spec.html)
[**id**](/html/attributes/id)
:   identifier text
[**hreflang**](/html/attributes/hreflang)
:   Language tag [for HTML5](http://www.ietf.org/rfc/bcp/bcp47.txt) or [for HTML4](http://www.ietf.org/rfc/rfc1766.txt)
[**rel**](/html/attributes/rel)
:   comma-separated list of keywords
[**target**](/html/attributes/target)
:   [Browsing context](http://www.w3.org/TR/html5/browsers.html#valid-browsing-context-name-or-keyword)

## Examples

``` {.html}
<!-- Link to an external website. -->
<a href="http://www.example.com">Example website</a>

<!-- Link to an internal website in same directory. -->
<a href="home.html">Home</a>

<!-- Download link (HTML5 only). Value of download attribute is used as pre-filled file name in Save dialog.
    If no value is specified for the download, the name of the resource will be used.-->
<a href="filename_on_server.pdf" download="meaningful_filename.pdf">Download your pdf</a>

<!-- Open a link in the window specified by the attribute TARGET. -->
<a href="http://www.example.com" target="_blank">Open example website in new window</a>

<!-- Include an IMG element as a part of the link. -->
<a href="http://www.example.com"><img src="images/bullet.png">A link with an image</a>

<!-- Link to an anchor on the same page. -->
<a href="#top">Go to top</a>

<!-- Define an anchor. -->
<a id="top"></a>

<!-- Invoke a JavaScript function (Not recommended) -->
<a href="javascript:alert('Link clicked')">Click this link</a>

<!-- Links to a document and uses the rel attribute to specify the relationship to the linked document. -->
<a href="http://www.example.com/help" rel="help">Link to help</a>
```

[View live example](http://code.webplatform.org/gist/5281100)

## Notes

### Remarks

For creating an anchor in the page, the [**name**](/html/attributes/name) attribute is obsolete and should be replaced by [**id**](/html/attributes/id) attribute.

Both text and images can be included within an anchor. An image that is an anchor has a border whose color indicates whether the link has been visited. To prevent this border from appearing, you can set the **img** element's [**border**](/html/attributes/border) attribute to 0 or omit the **border** attribute. You can also use CSS attributes to override the default appearance of **a** and **img** elements.

The URI may refer to any protocol, e.g. http, mailto, file. A fragment (\# followed by text) refers to a location in the current page. href may be omitted to indicate a placeholder link, such as a reference to the current page in a menu.

Optionally the [**rel**](/html/attributes/rel) element may be specified to provide semantic meaning to the link target.

Internationalization topics related to the `a` element:

-   [Indicating the language of a link destination](http://www.w3.org/International/techniques/authoring-html#linkdestination)

### Clicking and focus

Whether clicking on an anchor causes it to (by default) become focused varies by browser and OS.

Does clicking on an anchor give it the focus?

Desktop Browsers
:   Windows 8.1
Firefox 30.0
:   Yes
Chrome [\>=39](https://code.google.com/p/chromium/issues/detail?id=388666)
:   Yes
Safari 7.0.5
:   N/A
Internet Explorer 11
:   Yes
Presto (Opera 12)
:   Yes

Does tapping on an anchor give it the focus?

Mobile Browsers
:   iOS 7.1.2
Safari Mobile
:   Only when it has a [`tabindex`](/html/attributes/tabIndex)
Chrome 35
:   ???

Â

## Related specifications

Specification
:   Status
[HTML 5.1](http://www.w3.org/TR/html51/text-level-semantics.html#the-a-element)
:   W3C Working Draft
[HTML 5](http://www.w3.org/TR/html5/text-level-semantics.html#the-a-element)
:   W3C Recommendation
[HTML 4.01](http://www.w3.org/TR/html401/struct/links.html#edef-A)
:   W3C Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/HTML/Element/a)

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

