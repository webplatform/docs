---
title: body
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://test.w3.org/html/examples/elements/body/body01.html'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLBodyElement](/dom/HTMLBodyElement)'
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'The body element (&lt;body&gt;) represents the main content of the document.'
tags:
  - Markup
  - Elements
  - HTML
uri: html/elements/body

---
## <span>Summary</span>

The body element (&lt;body&gt;) represents the main content of the document.

## <span>Overview Table</span>

[DOM Interface](/dom/interface)
:   [HTMLBodyElement](/dom/HTMLBodyElement)

You can access the `<body>` element from script through the document object.

The window object for the `<body>` element can host event handlers for the `onblur`, `onfocus`, `onload`, or `onunload` events.

### <span>HTML Event Handler Content Attributes</span>

|Event|Description|
|:----|:----------|
|`onafterprint`|User printed current document.|
|`onbeforeprint`|User requested printing of current document.|
|`onbeforeunload`|Document is about to be unloaded.|
|`onblur`|Document lost focus.|
|`onerror`|Document failed to load properly.|
|`onfocus`|Document received focus.|
|`onhashchange`|Fragment identifier part of the document’s current address changed.|
|`onload`|Document finished loading.|
|`onmessage`|Document received a message.|
|`onoffline`|Network connections failed.|
|`ononline`|Network connections returned.|
|`onpopstate`|User navigated session history.|
|`onredo`|User went forward in undo transaction history.|
|`onresize`|Document view was resized.|
|`onstorage`|Storage area changed.|
|`onundo`|User went backward in undo transaction history.|
|`onunload`|Document is going away.|

The following attributes are obsolete, and should not be used by authors: `alink`, `bgcolor`, `link`, `marginbottom`, `marginheight`, `marginleft`, `marginright`, `margintop`, `marginwidth`, `text`, `vlink`.

## <span>Examples</span>

The `<body>` element follows the `<head>` element and is contained by the `<html>` element.

``` html


<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8">
<title>The HTML Document</title>
</head>
<body>
<p>The HTML content</p>
</body>
</html>
```

</pre>
[View live example](http://test.w3.org/html/examples/elements/body/body01.html)

This example exposes the `<body>` element in javascript.

``` js


var oBody = document.body;
```

</pre>

## <span>Related specifications</span>

[HTML 5.1](http://www.w3.org/TR/html51/sections.html#the-body-element)
:   W3C Working Draft

[HTML 5](http://www.w3.org/TR/html5/sections.html#the-body-element)
:   W3C Recommendation

[HTML 4.01](http://www.w3.org/TR/html401/struct/global.html#edef-BODY)
:   W3C Recommendation
