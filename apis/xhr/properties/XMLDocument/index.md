---
title: XMLDocument
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs summary, spec reference, standardization status'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Element
    href: /dom/Element
tags:
  - API
  - Object
  - Properties
  - DOM
uri: apis/xhr/properties/XMLDocument

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Property of [dom/Element](/dom/Element)[dom/Element](/dom/Element)

## <span>Syntax</span>

``` js
var result = element.XMLDocument;
element.XMLDocument = value;
```

## <span>Examples</span>

This example uses the **XMLDocument** property to access the object model of an **xml** data island.

``` html
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

## <span>Notes</span>

### <span>Remarks</span>

**XMLDocument** is the default property; specifying the property is optional. The **XMLDocument** property is useful when an entire XML document is passed to a method that requires an **html** element, instead of an **xml** element. The **XMLDocument** property provides access to the root of the XML tree in the data island. For a complete description of the XML DOM exposed by the **XMLDocument** property, see the XML DOM overview.

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `xml`
-   `Reference`
-   `XSLDocument`
-   `Conceptual`
-   `Introduction to Persistence`
