---
title: open
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'In Progress'
notes:
  - 'Needs summary and compat, and better spec links'
uri: dom/Document/open

---
# open

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

*Method of [dom/Document](/dom/Document)*

## Syntax

``` {.js}
var object = object.open(url, name, features, replace);
```

## Parameters

### url

 Data-typeÂ
:   any

### name

 Data-typeÂ
:   BSTR

**Note**Â Â The following applies only if this method is used instead of [**window.open**](/dom/Window/open).

### features

 Data-typeÂ
:   BSTR

**Note**Â Â The following applies only if this method is used instead of [**window.open**](/dom/Window/open).

### replace

 Data-typeÂ
:   any

## Return Value

Returns an object of type DOM Node.

Object

**document**

## Examples

The following example shows how to use the **open** method to replace the current document with a new document and display the HTML markup contained in the variable *sMarkup*.

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

## Notes

### Remarks

When a function fired by an event on any object calls the **open** method, the [**window.open**](/dom/Window/open) method is implied.

    <script language="JScript">
    function myOpen() {
        open('about:blank');}
    </script>
    <body onclick="myOpen();">
    Click this page and window.open() is called.
    </body>

### Syntax

### Standards information

-   [Document Object Model (DOM) Level 2 HTML Specification](http://go.microsoft.com/fwlink/p/?linkid=196991), Section 1.5
-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374), Section 3.4.1

## See also

### Related pages (MSDN)

-   `Reference`
-   `close`
-   `open`
-   `write`
-   `writeln`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

