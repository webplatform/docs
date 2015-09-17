---
title: 'iframe'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: iframe
  topic: html
notes:
  - "Add Category, Parent, Children and Compatibility information.\nNotes section is from MSDN and very IE-specific."
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLIFrameElement](/dom/HTMLIFrameElement)'
readiness: 'In Progress'
standardization_status: 'W3C Recommendation'
summary: 'The iframe element (&lt;iframe&gt;) introduces a new nested browsing context.'
tags:
  - Markup_Elements
  - HTML
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/properties/frames
uri: html/elements/iframe

---
## Summary

The iframe element (&lt;iframe&gt;) introduces a new nested browsing context.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLIFrameElement](/dom/HTMLIFrameElement)

Iframes are one the best ways to build up a complex, detailed webpage from smaller, more manageable chunks. By using iframe tags, a developer can include webpages as part of a larger, enompassing parent page. Unlike frames, iframes can be styled through CSS and easily molded to fit seamlessly within the parent page. One neat use of an iframe is to display a custom Google map within the page. This can be done by setting the 'src' attribute of the iframe tag to Google Map URL.

## HTML Attributes

-   `src` = URL potentially surrounded by spaces
    Gives the address of a page that the nested browsing context is to contain.
-   `srcdoc` = HTML contents
    Gives the content of the page that the nested browsing context is to contain.
-   `name` = browsing-context name
    Represents the browsing-context name. When the browsing context is created, if the attribute is present, the browsing context name must be set to the value of this attribute; otherwise, the browsing context name must be set to the empty string.
-   `sandbox` = allow-same-origin/ allow-top-navigation/ allow-forms/ allow-scripts
    Enables a set of extra restrictions on any content hosted by the iframe.
    -   If presents, given in the following list set.
        -   prevents content from navigating browsing contexts other than the sandboxed browsing context itself.
        -   prevents content from navigating their top-level browsing context.
        -   prevents content from instantiating plugins, whether using the embed element, the object element, the applet element, or through navigation of a nested browsing context.
        -   prevents content from using the seamless attribute on descendant iframe elements.
        -   forces content into a unique origin, thus preventing it from accessing other content from the same origin.
        -   blocks form submission, blocks script execution.
        -   blocks features that trigger automatically, such as automatically playing a video or automatically focusing a form control.
    -   `allow-same-origin`
        allows the content to be treated as being from the same origin instead of forcing it into a unique origin.
    -   `allow-top-navigation`
        allows the content to navigate its top-level browsing context
    -   `allow-forms` and `allow-scripts`
        re-enable forms and scripts respectively (though scripts are still prevented from creating popups).
-   `seamless` = boolean
    Indicates that the iframe element's browsing context is to be rendered in a manner that makes it appear to be part of the containing document (seamlessly included in the parent document).
-   `width` = non-negative integer
    Give the width of the visual content of the element, in CSS pixels.
-   `height` = non-negative integer
    Give the height of the visual content of the element, in CSS pixels.

## Examples

This example embeds `http://example.com/` via an IFrame element.

``` html
<iframe id="theFrame" src="http://example.com/"></iframe>
```

This example shows how to grab the Document contained within an IFrame element (note that you may only reach down into an IFrame if the page it has loaded is same-origin).

``` js
var frameDoc = document.getElementById("theFrame").contentDocument;
```

## Usage

     The developer should be careful not to overuse iframes, because they dramatically slow down the rendering of a page. For each extra iframe, the browser has to make an extra request to the server.

## Notes

### Remarks

The **iframe** element functions as a document within a document, or like a floating **frame**. The [**frames**](/w/index.php?title=dom/properties/frames&action=edit&redlink=1) collection provides access to the contents of an **iframe**. Use the **frames** collection to read or write to elements contained in an **iframe**. For example, the syntax for accessing the [**backgroundColor**](/css/properties/background-color) style of the **body** object in an **iframe** is:

    sColor = document.frames("sFrameName").document.body.style.backgroundColor;

You can access the **iframe** object's properties, but not its contents, through the object model of the page where the **iframe** object resides. For example, the syntax for accessing the [**border**](/css/properties/border) style of the **iframe** object is:

    sBorderValue = document.all.oFrame.style.border;

**Note**  Properties of the **iframe** must be accessed using the prefix, `document.all`, for example, `document.all.iframeId.marginWidth`.

**Security Warning:  ** To protect user privacy and safeguard your applications, Windows Internet Explorer restricts some interactions between frames that host Web pages from different domains. To treat the content of the **iframe** as if it were in the Restricted Sites zone, set the **SECURITY** attribute to "restricted." For more information about using the Dynamic HTML (DHTML) object model with the **frame** and **iframe** objects, see About Cross-Frame Scripting and Security and Security Considerations: Dynamic HTML. Windows Internet Explorer 8 and later. The values of the [**longDesc**](/html/attributes/longDesc) and [**src**](/html/attributes/src_(iframe,_embed,_xml)) attributes depend on the current document compatibility mode. Windows Internet Explorer 7 and later. For security reasons, resizing is disabled for **iframe** objects that display content hosted on a domain different from the domain hosting the parent document. If you trust the content you are loading into an **iframe** object, you can enable resizing by specifying values for the [**minWidth**](/css/properties/min-width) and [**maxWidth**](/css/properties/max-width) attributes of the **iframe** element in the source of the parent document. You must specify values for both attributes to enable resizing. Microsoft Internet Explorer 5.5 supports transparent content with inline floating frames. The following conditions must be met to define transparent content for inline floating frames.

1.  The [**allowTransparency**](/html/attributes/allowTransparency) attribute, used with the **iframe** element, must be set to `true`.
2.  In the **iframe** content source document, the [**backgroundColor**](/css/properties/background-color) attribute of the **body** element must be set to `transparent`.

Using Transparency with Inline Floating Frames

## Related specifications

[HTML 5.1](http://www.w3.org/TR/html51/embedded-content.html#the-iframe-element)
:   W3C Working Draft

[HTML 5](http://www.w3.org/TR/html5/embedded-content-0.html#the-iframe-element)
:   W3C Recommendation

[HTML 4.01](http://www.w3.org/TR/html401/present/frames.html#edef-IFRAME)
:   W3C Recommendation

## See also

### External resources

<http://www.w3.org/TR/html-markup/iframe.html#iframe>

### Related pages

-   `Using IFRAME Elements`
