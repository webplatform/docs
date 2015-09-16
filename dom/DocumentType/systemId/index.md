---
title: systemId
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs summary and compat tables, also better spec link'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/DocumentType
    href: /dom/DocumentType
standardization_status: 'W3C Recommendation'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/DocumentType/systemId

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Property of [dom/DocumentType](/dom/DocumentType)[dom/DocumentType](/dom/DocumentType)

## Syntax

``` js
var result = element.systemId;
element.systemId = value;
```

## Examples

The following example shows the **systemId** property with respect to a [!DOCTYPE](/html/elements/!DOCTYPE) directive.

``` html
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
  "http://www.w3.org/TR/html4/strict.dtd">
<html>
<head>
  <title>IE9 Doctype Sample: SystemId</title>
  <meta name="x-ua-compatible" content="ie=9">
  <script type="text/javascript">
  function showInfo() {
    var s = document.doctype.systemId;
    // Displays "http://www.w3.org/TR/html4/strict.dtd"
    alert( s );
  }
  </script>
  </head>
  <body>
  <button onclick="showInfo();">Click Me!</button>
  </body>
</html>
```

## Notes

### Remarks

The value of the **systemId** property corresponds to the *URL* attribute of a [!DOCTYPE](/html/elements/!DOCTYPE) directive.

### Syntax

### Standards information

-   [Document Object Model (DOM) Level 3 Core Specification](http://go.microsoft.com/fwlink/p/?linkid=182717), Section 1.5

## See also

### Related pages

-   `DocumentType`
-   `name`
-   `publicId`
