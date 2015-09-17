---
title: 'codeBase'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: codeBase
  topic: html
notes:
  - 'Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info'
readiness: 'Not Ready'
summary: 'Sets or retrieves the URL of the component.'
tags:
  - Markup_Attributes
  - HTML
uri: html/attributes/codeBase

---
## Summary

Sets or retrieves the URL of the component.

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

The following example uses the **CODEBASE** attribute to specify the download location of the Common Dialog control.

``` html
<OBJECT ID="CommonDialog1" WIDTH=32 HEIGHT=32
    CLASSID="CLSID:F9043C85-F6F2-101A-A3C9-08002B2F49FB"
    CODEBASE="http://activex.microsoft.com/controls/vb5/comdlg32.cab
    #Version=1,0,0,0">
</OBJECT>
```

## Notes

### Remarks

Applets do not support version information supplied as part of the URL. If *a*, *b*, *c*, and *d* are all set to `-1` (\#Version=-1,-1,-1,-1), the component is downloaded from the server if the release date is later than the installation date on the client computer. If the component is installed on the client computer and the release date is the same or earlier than the installation date, only an HTTP header transaction occurs. The URL of the component cannot be a local path. Windows Internet Explorer 8 or later. In IE8 Standards mode, the value of the **codeBase** attribute depends on the context of the reference to the attribute. When read as a Document Object Model (DOM) attribute, **codeBase** returns an absolute URL. The value specified by the page author is returned when **codeBase** is read as a content attribute, when the page is displayed in an earlier document compatibility mode, or when the page is viewed with an earlier version of the browser. For more information, see Attribute Differences in Internet Explorer 8.

### Syntax

## See also

### Related pages

-   `applet`
-   `object`
-   `Managing Versions of a Component`
