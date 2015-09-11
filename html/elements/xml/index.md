---
title: xml
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLElement](/dom/HTMLElement)'
readiness: 'Not Ready'
standardization_status: Non-Standard
summary: 'Defines a simple XML data that can be embedded directly in an HTML page.'
tags:
  - Pages
  - using
  - duplicate
  - arguments
  - in
  - template
  - calls
  - Markup
  - Elements
  - HTML
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - 'dom/properties/readyState (Link, Img, Input, Style...elements)'
uri: html/elements/xml

---
## <span>Summary</span>

Defines a simple XML data that can be embedded directly in an HTML page.

## <span>Overview Table</span>

[DOM Interface](/dom/interface)
:   [HTMLElement](/dom/HTMLElement)

## <span>Examples</span>

This example uses the **XML** element to define a simple XML data island that can be embedded directly in an HTML page.

``` html
<XML ID="oMetaData">
  <METADATA>
     <AUTHOR>John Smith</AUTHOR>
     <GENERATOR>Visual Notepad</GENERATOR>
     <PAGETYPE>Reference</PAGETYPE>
     <ABSTRACT>Specifies a data island</ABSTRACT>
  </METADATA>
</XML>
```

This example uses the [**readyState**](/w/index.php?title=dom/properties/readyState_(Link,_Img,_Input,_Style...elements)&action=edit&redlink=1) property of the **xml** object to determine whether the XML data island is completely downloaded.

``` html
if (oMetaData.readyState == "complete")
      window.alert ("The XML document is ready.");
```

This example uses the **readyState** property of the **XMLDOMDocument** object to determine whether the XML data island is completely downloaded.

``` html
if (oMetaData.XMLDocument.readyState == 4)
      window.alert ("The XML document is ready.");
```

This script example retrieves the text contained within the **ABSTRACT** field of the data island.

``` html
var oNode = oMetaData.XMLDocument.selectSingleNode("METADATA/ABSTRACT");
   alert(oNode.text);
```

## <span>Notes</span>

### <span>Remarks</span>

The [**readyState**](/w/index.php?title=dom/properties/readyState_(Link,_Img,_Input,_Style...elements)&action=edit&redlink=1) property of the **XML** element, available as a string value, corresponds to the **readyState** property of the **XMLDOMDocument** object, which is available as a long value. The string values correspond to the long values of the XML document object's property as shown in the Examples section. The [**XMLDocument**](/apis/xhr/properties/XMLDocument) property is the default property. This element is available in HTML and script as of Microsoft Internet Explorer 5.

### <span>Standards information</span>

There are no standards that apply here.

### <span>Members</span>

The **xml** object has these types of members:

-   [\#events Events]
-   [\#methods Methods]
-   [\#properties Properties]

#### <span>Events</span>

The **xml** object has these events. {