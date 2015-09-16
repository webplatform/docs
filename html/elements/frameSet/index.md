---
title: 'frameSet'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: frameSet
  topic: html
notes:
  - 'Deletion Candidate: It''s deprecated, http://www.w3.org/TR/html5/obsolete.html#non-conforming-features'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLFrameSetElement](/dom/HTMLFrameSetElement)'
readiness: 'Not Ready'
standardization_status: Deprecated
summary: "The frameset element (&lt;frameset&gt;) defines a collection of frames.\nThe &lt;frameset&gt; element holds one or more &lt;frame&gt; elements. Each &lt;frame&gt; element can hold a separate document.\nThe &lt;frameset&gt; tag is obsolete in HTML5.\n"
tags:
  - Markup
  - Elements
  - HTML
uri: html/elements/frameSet

---
## Summary

The frameset element (&lt;frameset&gt;) defines a collection of frames. The &lt;frameset&gt; element holds one or more &lt;frame&gt; elements. Each &lt;frame&gt; element can hold a separate document. The &lt;frameset&gt; tag is obsolete in HTML5.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLFrameSetElement](/dom/HTMLFrameSetElement)

## Examples

This example uses the **FRAMESET** element to define three columns of rectangular frames in a document.

``` html
<FRAMESET COLS="25%, 50%, *">
<FRAME SRC="contents.htm">
<FRAME SRC="info.htm">
<FRAME SCROLLING="NO" SRC="graphic.htm">
</FRAMESET>
```

## Notes

### Remarks

The **FRAMESET** element is a container for the **FRAME** element. An HTML document can contain either the **FRAMESET** element or the **BODY** element, but not both. If a user opens a folder inside a frame and then clicks something in the folder, the file or folder that the user clicks takes over the entire window. For example, suppose that a page contains two frames, one frame pointing to <http://www.microsoft.com> and the second frame pointing to a network drive. If the user clicks a file or folder in the second frame, that frame takes control of the entire window, including the first frame. For file types that the application cannot host, such as .txt files, a separate window in the appropriate host application is opened. A folder is a part of the file system hierarchy, but it does not necessarily represent anything in the file system. An example is Network Neighborhood. **Security Warning:  ** To protect user privacy and safeguard your applications, Windows Internet Explorer restricts some interactions between frames that host Web pages from different domains. For more information about using the Dynamic HTML (DHTML) object model with the **frame** and **iframe** objects, see About Cross-Frame Scripting and Security and Security Considerations: Dynamic HTML.

## See also

### Related pages

-   `frame`
