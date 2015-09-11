---
title: applet – obsolete
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Deletion Candidate: It''s deprecated, http://www.w3.org/TR/html5/obsolete.html#non-conforming-features'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLAppletElement](/dom/HTMLAppletElement)'
readiness: 'Not Ready'
standardization_status: Deprecated
summary: 'The applet element (&lt;applet&gt;) embeds a Java applet into a web page.'
tags:
  - Markup
  - Elements
  - HTML
uri: html/elements/applet

---
## <span>applet</span>

For technical reasons, the title of this article is not the text used to call this API. Instead, use `applet`

## <span>Summary</span>

The applet element (&lt;applet&gt;) embeds a Java applet into a web page.

## <span>Overview Table</span>

[DOM Interface](/dom/interface)
:   [HTMLAppletElement](/dom/HTMLAppletElement)

The **applet** element has been deprecated with HTML 4.01 and made *obsolete* with HTML5.

## <span>Examples</span>

The following example shows how to embed Java applet 'myApplet' into a web page.

``` html
<applet code="myApplet.class" width="500" height="500">
My Java applet goes here!
</applet>
```

## <span>Notes</span>

### <span>Remarks</span>

To use executable content specified by the **applet** element, a user's computer must have a Java Runtime Environment (JRE) solution installed.

## <span>Related specifications</span>

[HTML 4.01](http://www.w3.org/TR/REC-html40/struct/objects.html#h-13.4)
:   W3C Recommendation

[HTML5](http://www.w3.org/TR/html5/obsolete.html#the-applet-element)
:   W3C Candidate Recommendation
