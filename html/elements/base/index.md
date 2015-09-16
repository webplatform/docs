---
title: base
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLBaseElement](/dom/HTMLBaseElement)'
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'The base element is used to specify a document''s base URL and base target that is used for resolving URI references (relative URLs) within the document.'
tags:
  - Markup
  - Elements
  - HTML
uri: html/elements/base

---
## Summary

The base element is used to specify a document's base URL and base target that is used for resolving URI references (relative URLs) within the document.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLBaseElement](/dom/HTMLBaseElement)

<table class="wikitable">
<tr>
<th style="vertical-align: top" id="permitted-contents">
Permitted contents

</th>
<td style="vertical-align: top; padding-top: 10px">
*none*

</td>
</tr>
<tr>
<th id="permitted-parents">
Permitted parents

</th>
<td>
Only permitted to occur once within [`<head>`](/html/elements/head).

</td>
</tr>
</table>
A relative URL (<var>some/example.html</var>) needs to be transformed to a fully qualified URL (<var><http://example.org/some/example.html></var>) before it can be downloaded. Usually the document's URL (available to JavaScript through the [`location`](/dom/Location) object) is used as the base URL for resolving relative URLs. The `<base>` element allows you to override this default with the [`href`](/html/attributes/href) attribute.

Links ([`<a>`](/html/elements/a)) and forms ([`<form>`](/html/elements/form)) open in a ([`target`](/html/attributes/target)). The default target is <var>\_self</var>, resulting in the link opening in the same window as the document currently viewed. This default can be overridden document-wide using `<base target="…">`.

If a document is integrated in an [`iframe`](/html/elements/iframe), it may help to specify `<base target="_parent">` in order to open the links within the iframe in the scope parent document. If <var>\_parent</var> or <var>\_top</var> are used without the document really being integrated in an hierarchy, expect the behavior of <var>\_self</var>.

## HTML Attributes

-   `href` = URI, potentially surrounded by spaces
    A base element, if it has an href attribute, must come before any other elements in the tree that have attributes defined as taking URLs, except the html element (its manifest attribute isn't affected by base elements). [[Example A]](#Example_A)

-   `target` = browsing context name or keyword ( \_blank, \_self, \_parent, or \_top)
    The value of the target attribute is used as the default when hyperlinks and forms in the Document cause navigation.

## Examples

The example shows a link with the relative destination <var>some-file.html</var> that gets rewritten to <var><http://example.org/deep/some-file.html></var>

``` html
<!DOCTYPE html>
<html>
  <head>
    <title>base element example</title>
    <base href="http://www.example.org/deep/">
  </head>
  <body>
    <p>A <a href="some-file.html">relative link</a>.</p>
    <!-- after resolving the above link equals to -->
    <p>A <a href="http://www.example.org/deep/some-file.html">relative link</a>.</p>
  </body>
</html>
```

The example shows that **base** only affects elements following it

``` html
<head>
  <title>base element example</title>
  <link href="my-style.css" rel="stylesheet">
  <base href="http://example.com">
  <link href="my-other-style.css" rel="stylesheet">
  <!--
    resolves to
    [current domain and directory]/my-style.css
    http://example.com/my-other-style.css
  -->
</head>
```

The example shows how multiple **base** occurrences are collapsed and ignored

``` html
<head>
  <title>base element example</title>
  <base href="http://example.com">
  <base target="_blank">
  <base href="http://webplatform.org" target="_top">
  <!--
    equals to the single definition:
    <base href="http://example.com/" target="_blank">
    except for Internet Explorer, where only the first element is read:
    <base href="http://example.com/" target="_self">
  -->
</head>
```

## Notes

-   Relative URLs within `<base>` don't work in every browser, resolving a relative base URL was introduced in Firefox 4 and Internet Explorer 10.
-   `<base>` only affects elements following it's declaration.
-   multiple `<base>` declarations are illegal, only the *first* [`href`](/html/attributes/href) and [`target`](/html/attributes/target) are used, the rest is discarded. Internet Explorer ignores all `<base>` instances after the first.

**Note** Inline SVGs using references like `fill="url(#element-id)"` can be a problem in documents using `<base>`. The reason is that `url(#element-id)` is actually a URL, not a CSS selector. At least Firefox and Chrome are susceptible to this behavior.

## Related specifications

[HTML 5.1](http://www.w3.org/TR/html51/document-metadata.html#the-base-element)
:   W3C Working Draft

[HTML 5](http://www.w3.org/TR/html5/document-metadata.html#the-base-element)
:   W3C Recommendation

[HTML 4.01](http://www.w3.org/TR/html401/struct/links.html#edef-BASE)
:   W3C Recommendation

## See also

### External resources

-   [Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/HTML/Element/base)
-   [Microsoft Developer Network](http://msdn.microsoft.com/en-us/library/ie/ms535191%28v=vs.85%29.aspx)
