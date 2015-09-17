---
title: 'name'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs summary and compat and better spec link'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/DocumentType
    href: /dom/DocumentType
standardization_status: 'W3C Recommendation'
tags:
  - API_Object_Properties
  - DOM
  - Needs_Summary
uri: dom/DocumentType/name

---
Property of [dom/DocumentType](/dom/DocumentType)[dom/DocumentType](/dom/DocumentType)

## Syntax

``` js
var result = element.name;
element.name = value;
```

## Examples

The following example shows the **name** property with respect to a [!DOCTYPE](/html/elements/!DOCTYPE) directive.

``` html
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
```

## Notes

### Remarks

The value of the **name** property corresponds to the *TopElement* attribute of a [!DOCTYPE](/html/elements/!DOCTYPE) directive.

### Syntax

### Standards information

-   [Document Object Model (DOM) Level 3 Core Specification](http://go.microsoft.com/fwlink/p/?linkid=182717), Section 1.5

## See also

### Related pages

-   DocumentType[DocumentType](/dom/DocumentType)
-   publicId[publicId](/dom/DocumentType/publicId)
-   systemId[systemId](/dom/DocumentType/systemId)
