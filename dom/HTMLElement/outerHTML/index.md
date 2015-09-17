---
title: 'outerHTML'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'summary, clean-up of MSDN import'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/HTMLElement
    href: /dom/HTMLElement
tags:
  - API_Object_Properties
  - DOM
  - Needs_Summary
uri: dom/HTMLElement/outerHTML

---
Property of [dom/HTMLElement](/dom/HTMLElement)[dom/HTMLElement](/dom/HTMLElement)

## Syntax

``` js
var result = element.outerHTML;
element.outerHTML = value;
```

## Examples

This example uses the **outerHTML** property to copy an object, accompanying attributes, and children to a list when a user clicks one of the objects.

``` html
<SCRIPT>
function fnCopyHTML(){
   var oWorkItem = event.srcElement;
   if((oWorkItem.tagName != "UL") && (oWorkItem.tagName != "LI")){
      alert("Adding " + oWorkItem.outerHTML + " to the list.");
      oScratch.innerHTML += oWorkItem.outerHTML + "<BR>";
   }
}
</SCRIPT>

<UL onclick = "fnCopyHTML()">
<LI><B>Bold text</B>
<LI><I>Italic text</I>
<LI><U>Underlined text</U>
<LI><STRIKE>Strikeout text</STRIKE>
</UL>
<P>
<DIV ID = "oScratch" >
</DIV>
```

## Notes

### Remarks

The **outerHTML** property is read-only on the **caption**, **col**, **colGroup**, **html**, **head**, **body**, **frameSet**, **tBody**, **td**, **tFoot**, **th**, **tHead**, and **tr** objects. The property can be any valid string containing a combination of text and tags. When the property is set, the given string completely replaces the object, including its start and end tags. If the string contains HTML tags, the string is parsed and formatted as it is placed into the document. You can set this property only after the [**onload**](/dom/Element/load) event fires on the **window**. When dynamically creating a tag using [**TextRange**](/dom/TextRange), [**innerHTML**](/dom/HTMLElement/innerHTML), or **outerHTML**, use script to create new events to handle the newly formed tags. Microsoft Visual Basic Scripting Edition (VBScript) is not supported. You can change the value of the **title** element using the [**title**](/html/elements/title) property. To change the contents of the [**table**](/html/elements/table), **tFoot**, **tHead**, and **tr** elements, use the table object model. For example, use the [**rowIndex**](/dom/HTMLElement/rowIndex) property or the [**rows**](/dom/HTMLElement/rows) collection to retrieve a reference to a specific table row. You can add or delete rows using the [**insertRow**](/dom/HTMLTableElement/insertRow) and [**deleteRow**](/dom/HTMLTableElement/deleteRow) methods. To retrieve a reference to a specific cell, use the [**cellIndex**](/dom/HTMLElement/cellIndex) property or the [**cells**](/dom/HTMLTableElement/cellSpacing) collection. You can add or delete rows using the [**insertCell**](/dom/HTMLTableElement/insertCell) and [**deleteCell**](/dom/HTMLTableElement/deleteCell) methods. To change the content of a particular cell, use the [**innerHTML**](/dom/HTMLElement/innerHTML) property. This property is accessible at run time as of Microsoft Internet Explorer 5. Removing elements at run time, before the closing tag has been parsed, can prevent other areas of the document from rendering.

### Syntax
