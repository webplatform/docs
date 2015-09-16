---
title: href
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info'
readiness: 'Not Ready'
summary: 'Sets or retrieves a destination URL or an anchor point'
tags:
  - Markup
  - Attributes
  - HTML
uri: html/attributes/href

---
## Summary

Sets or retrieves a destination URL or an anchor point

<table class="wikitable">
<tr>
<th>
Applies to

</th>
<td>
 ?

</td>
</tr>
</table>
## Examples

Using `a` and `href` to link to the top-level page in the same domain.

``` html
<a href="/">Home</a>
```

This example function returns the [**href**](/css/cssom/properties/href) property of the current page location.

``` js
function getHref()
{
    return document.location.href;
}
```

Using `a` and `href` to link to an email address.

``` html
<a href="mailto:bigcheese@webplatform.org">Email</a>
```

Using `a` and `href` to link to a telephone number.

``` html
<a href="tel:5555551212">Call us!</a>
```

## Notes

### Remarks

When specified for an [**a**](/html/elements/a) element (also called an *anchor element*), **HREF** defines a link to another document or another location within the document containing the **a** element. By default, the text between the opening and closing tags of the anchor element is underlined and the location specified by the **HREF** attribute is loaded when the user activates the link.

**Note**  You can use the Cascading Style Sheets (CSS) style rules to modify the appearance of anchor elements. The value of the **HREF** can be a URL that loads a separate document when the link is activated, or a fragment identifier. Fragment identifiers, or*bookmarks*, define target locations within a document that are brought into view when links are activated. Use the [**NAME**](/html/attributes/name_(frames)) attribute of a separate anchor element to define a bookmark as a target location within a document.

**Note**  Generally, relative URLs are resolved against the location of the document containing the [**a**](/html/elements/a) element. You can use the **base** element to control the resolution of relative URLs. For more information on standard Internet protocols such as ftp, http, and mailto, see Predefined Protocols. The **img** element does not support the **HREF** content attribute. In addition, the **href** property is read-only for the **img** Document Object Model (DOM) object. If **HREF** is specified as a blank value (`href=""` or `href=`), executing the link might display the directory containing the current document, or it might generate an error, depending on other elements in the document and the server environment. Windows Internet Explorer 8 or later. In IE8 Standards mode, the value of the **HREF** depends on the context of the reference to the attribute. When read as a DOM attribute, **HREF** returns a URL relative to the domain hosting the Web page. **HREF** returns the value specified by the page author when read as a content attribute when the page is displayed in an earlier document compatibility mode, or when the page is viewed with an earlier version of the browser. For more information, see Attribute Differences in Internet Explorer 8. Internet Explorer 8 and later. When Protected Mode is enabled and a Web page contains an [**anchor link**](/html/elements/a) with a named [**target**](/html/attributes/target), Windows Internet Explorer opens the target of the link in a new window when the target has a different integrity level than the Web page containing the link. For more information, see Understanding and Working in Protected Mode Internet Explorer.

**Note**  As of Microsoft Internet Explorer 6 Service Pack 1 (SP1), browsing a local machine from the Internet zone is not allowed. For example, if an Internet site contains a link to a local file, Internet Explorer 6 SP1 and later displays a blank page when a user clicks on the link. Previous versions of Windows Internet Explorer followed the link to the local file.

### Standards information

-   [Document Object Model (DOM) Level 1 Specification](http://go.microsoft.com/fwlink/p/?linkid=161725), Section 2.5.5
-   [HTML 4.01 Specification](http://go.microsoft.com/fwlink/p/?linkid=25320), Section 12.2

## See also

### Related pages

-   `a`
-   `area`
-   `img`
-   `link`
