---
title: name
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'In Progress'
standardization_status: 'W3C Recommendation'
notes:
  - 'Needs summary and compat and better spec link'
uri: dom/DocumentType/name

---
# name

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/DocumentType](/dom/DocumentType)</span></span>

## Syntax

``` {.js}
var result = element.name;
element.name = value;
```

## Examples

The following example shows the **name** property with respect to a [!DOCTYPE](/html/elements/!DOCTYPE) directive.

    <!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
      "http://www.w3.org/TR/html4/strict.dtd">
    <html>
    <head>
      <title>IE9 Doctype Sample: Name</title>
      <meta name="x-ua-compatible" content="ie=9">
      <script type="text/javascript">
      function showInfo() {
        var s = document.doctype.name;
        // Displays "HTML"
        alert( s );
      }
      </script>
      </head>
      <body>
      <button onclick="showInfo();">Click Me!</button>
      </body>
    </html>

## Notes

### Remarks

The value of the **name** property corresponds to the *TopElement* attribute of a [!DOCTYPE](/html/elements/!DOCTYPE) directive.

### Syntax

### Standards information

-   [Document Object Model (DOM) Level 3 Core Specification](http://go.microsoft.com/fwlink/p/?linkid=182717), Section 1.5

## See also

### Related pages (MSDN)

-   `DocumentType`
-   `publicId`
-   `systemId`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

