---
title: doctype
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs mobile compat table'
readiness: 'Almost Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Document
    href: /dom/Document
  return:
    predicate: 'Returns an object of type '
    value: 'DOM Node'
    href: /dom/Document
standardization_status: 'W3C Recommendation'
summary: 'Gets an object that represents the document type declaration that is associated with the current document.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/Document/doctype

---
## Summary

Gets an object that represents the document type declaration that is associated with the current document.

Property of [dom/Document](/dom/Document)[dom/Document](/dom/Document)

## Syntax

**Note**: This property is read-only.

``` js
var doctype = document.doctype;
```

## Return Value

Returns an object of type DOM NodeDOM Node

The DocumentType instance object of the document.

## Examples

This example retrieves the document's DOCTYPE and displays some of its available components.

``` html
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

[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/core.html#i-Document)
:   Recommendation
