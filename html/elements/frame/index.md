---
title: 'frame'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: frame
  topic: html
notes:
  - 'Deletion Candidate: It''s deprecated, http://www.w3.org/TR/html5/obsolete.html#non-conforming-features'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLFrameElement](/dom/HTMLFrameElement)'
readiness: 'Not Ready'
standardization_status: Deprecated
summary: "The frame element (&lt;frame&gt;) defines one particular window (frame) within a &lt;frameSet&gt;.\nThe &lt;frame&gt; element is obsolete in HTML5.\n"
tags:
  - Markup_Elements
  - HTML
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - html/elements/frameset
uri: html/elements/frame

---
## Summary

The frame element (&lt;frame&gt;) defines one particular window (frame) within a &lt;frameSet&gt;. The &lt;frame&gt; element is obsolete in HTML5.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLFrameElement](/dom/HTMLFrameElement)

## Examples

This example uses the **frame** element to define properties of the frame, including the location of the page loaded by the frame.

``` html
<frame frameborder=0 scrolling="no" src="sample.htm">
```

This example shows how to reference an object with`ID=sID` in `FRAME2`, from another frame of the same frameset.

``` html
parent.frames.FRAME2.sID.innertext
```

## Notes

### Remarks

You can access the **frame** object's properties (but not its contents) through the object model of the page in which the **frame** object resides. For example, the syntax for accessing the [**border**](/css/properties/border) style of the **frame** object is:

    sBorderValue = document.all.oFrame.style.border;

If a user opens a Web folder inside a frame and then clicks something in the Web folder, the file or folder that the user clicks takes over the entire window. For example, suppose that a page contains two frames, one frame pointing to <http://www.microsoft.com> and the second frame pointing to a network drive. If the user clicks a file or folder in the second frame, that frame takes control of the entire window, including the first frame. For file types that the browser cannot host, such as .txt files, a separate window in the appropriate host application is opened. A Web folder is a part of the file system hierarchy, but it does not necessarily represent anything in the file system. An example is Network Neighborhood.

**Security Warning:  ** To protect user privacy and safeguard your applications, Windows Internet Explorer restricts some interactions between frames that host Web pages from different domains. For more information about using the Dynamic HTML (DHTML) object model with the **frame** and **iframe** objects, see About Cross-Frame Scripting and Security and Security Considerations: Dynamic HTML. Windows Internet Explorer 8 and later. The values of the [**longDesc**](/html/attributes/longDesc) and [**src**](/html/attributes/src_(iframe,_embed,_xml)) attributes depend on the current document compatibility mode. Windows Internet Explorer 7 and later. For security reasons, resizing is disabled for **frame** objects that display content hosted on a domain different from the domain hosting the parent document. If you trust the content you are loading into an **frame** object, you can enable resizing by specifying values for the [**minWidth**](/css/properties/min-width) and [**maxWidth**](/css/properties/max-width) attributes of the **frame** element in the source of the parent document. You must specify values for both attributes to enable resizing. Microsoft Internet Explorer 5.5 supports transparent content for a **frame**. The following conditions must be met to define transparent content for a **frame**.

1.  The [**allowTransparency**](/html/attributes/allowTransparency) attribute, used with the **frame** element, must be set to VARIANT\_TRUE.
2.  In the **frame** content source document, the [**backgroundColor**](/css/properties/background-color) or [**bgColor**](/html/attributes/bgColor) attribute of the **body** element must be set to `transparent`.

## See also

### Related pages

-   `frameSet`
