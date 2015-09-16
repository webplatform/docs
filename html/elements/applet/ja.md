---
title: applet – obsolete
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
lang: ja
notes:
  - 'Deletion Candidate: It''s deprecated, http://www.w3.org/TR/html5/obsolete.html#non-conforming-features'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLAppletElement](/dom/HTMLAppletElement)'
readiness: 'Not Ready'
standardization_status: Deprecated
summary: '&lt;applet&gt;はJavaアプレットをウェブページに埋め込む際に使用します。'
tags:
  - Markup
  - Elements
  - HTML
uri: html/elements/applet/ja

---
## applet

For technical reasons, the title of this article is not the text used to call this API. Instead, use `applet`

## Summary

&lt;applet&gt;はJavaアプレットをウェブページに埋め込む際に使用します。

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLAppletElement](/dom/HTMLAppletElement)

**\<applet\>**要素はHTML4.01で非推奨となり、*HTML5の登場でほとんど使われなくなりました*。

## Examples

以下はウェブページに「myApplet」というJavaアプレットを埋め込む例です。

``` html
<applet code="myApplet.class" width="500" height="500">
My Java applet goes here!
</applet>
```

## Notes

### 備考

**\<applet\>**要素でJavaアプレットを実行する場合、ユーザのPCにJavaランタイム環境（JRE)がインストールされている必要があります。

## Related specifications

[HTML 4.01](http://www.w3.org/TR/REC-html40/struct/objects.html#h-13.4)
:   W3C Recommendation

[HTML5](http://www.w3.org/TR/html5/obsolete.html#the-applet-element)
:   W3C Candidate Recommendation
