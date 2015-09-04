---
title: XMLDocument
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'In Progress'
notes:
  - 'Needs summary, spec reference, standardization status'
uri: apis/xhr/properties/XMLDocument

---
# XMLDocument

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Element](/dom/Element)</span></span>

## Syntax

``` {.js}
var result = element.XMLDocument;
element.XMLDocument = value;
```

## Examples

This example uses the **XMLDocument** property to access the object model of an **xml** data island.

``` {.html}
<SCRIPT>
function fnCheck(){
   var oNode = oMetaData.XMLDocument.selectSingleNode
       ("METADATA/ABSTRACT");
   alert(oNode.text);
}
</SCRIPT>

<XML ID="oMetaData">
  <METADATA>
     <AUTHOR>John Smith</AUTHOR>
     <GENERATOR>Visual Notepad</GENERATOR>
     <PAGETYPE>Reference</PAGETYPE>
     <ABSTRACT>Specifies a data island</ABSTRACT>
  </METADATA>
</XML>

<INPUT TYPE=button VALUE="Test" onclick="fnCheck()">
```

## Notes

### Remarks

**XMLDocument** is the default property; specifying the property is optional. The **XMLDocument** property is useful when an entire XML document is passed to a method that requires an **html** element, instead of an **xml** element. The **XMLDocument** property provides access to the root of the XML tree in the data island. For a complete description of the XML DOM exposed by the **XMLDocument** property, see the XML DOM overview.

## See also

### Related pages (MSDN)

-   `xml`
-   `Reference`
-   `XSLDocument`
-   `Conceptual`
-   `Introduction to Persistence`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

