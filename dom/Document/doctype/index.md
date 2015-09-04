---
title: doctype
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Almost Ready'
standardization_status: 'W3C Recommendation'
notes:
  - 'Needs mobile compat table'
summary: 'Gets an object that represents the document type declaration that is associated with the current document.'
uri: dom/Document/doctype

---
# doctype

## Summary

Gets an object that represents the document type declaration that is associated with the current document.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Document](/dom/Document)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var doctype = document.doctype;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">DOM Node</span></span>

The DocumentType instance object of the document.

## Examples

This example retrieves the document's DOCTYPE and displays some of its available components.

``` {.html}
<!DOCTYPE HTML PUBLIC "-//W3C//DTD XHTML 1.1//EN" "http://www.w3.org/TR/xhtml11/DTD/xhtml11.dtd">
<html>
<head>
  <script type="text/javascript">
    function getDocType () {
      if (document.doctype) {
          var dtinfo = "DOCTYPE name: " + document.doctype.name;
          dtinfo += "\nDOCTYPE publicId: " + document.doctype.publicId;
          dtinfo += "\nDOCTYPE systemId: " + document.doctype.systemId;
          alert(dtinfo);
      }
      else {
          alert ("Your browser does not support this example");
      }
    }
  </script>
</head>
<body>
  <button onclick="getDocType();">View DOCTYPE information</button>
</body>
</html>
```

## Related specifications

Specification
:   Status
[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/core.html#i-Document)
:   Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

