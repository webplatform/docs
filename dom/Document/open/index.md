---
title: open
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs summary and compat, and better spec links'
readiness: 'In Progress'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Document
    href: /dom/Document
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /dom/Document
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/Document/open

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Method of [dom/Document](/dom/Document)[dom/Document](/dom/Document)

## <span>Syntax</span>

``` js
var object = object.open(url, name, features, replace);
```

## <span>Parameters</span>

### <span>url</span>

 Data-type
:   any

### <span>name</span>

 Data-type
:   BSTR

**Note**  The following applies only if this method is used instead of [**window.open**](/dom/Window/open).

### <span>features</span>

 Data-type
:   BSTR

**Note**  The following applies only if this method is used instead of [**window.open**](/dom/Window/open).

### <span>replace</span>

 Data-type
:   any

## <span>Return Value</span>

Returns an object of type DOM NodeDOM Node

Object

**document**

## <span>Examples</span>

The following example shows how to use the **open** method to replace the current document with a new document and display the HTML markup contained in the variable *sMarkup*.

``` html
<html>
<head>
<title>First Document</title>
<script>
function replace(){
    var oNewDoc = document.open("text/html", "replace");
    var sMarkup = "<html><head><title>New Document</title></head><body>Hello, world</body></html>";
    oNewDoc.write(sMarkup);
    oNewDoc.close();
}
</script>
</head>
<body>
<h1>I just want to say</h1><br>
<!--Button will call the replace function and replace the current page with a new one-->
<input type ="button" value = "Finish Sentence" onclick="replace();">
</body>
</html>
```

## <span>Notes</span>

### <span>Remarks</span>

When a function fired by an event on any object calls the **open** method, the [**window.open**](/dom/Window/open) method is implied.

    <script language="JScript">
    function myOpen() {
        open('about:blank');}
    </script>
    <body onclick="myOpen();">
    Click this page and window.open() is called.
    </body>

### <span>Syntax</span>

### <span>Standards information</span>

-   [Document Object Model (DOM) Level 2 HTML Specification](http://go.microsoft.com/fwlink/p/?linkid=196991), Section 1.5
-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374), Section 3.4.1

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `Reference`
-   `close`
-   `open`
-   `write`
-   `writeln`
