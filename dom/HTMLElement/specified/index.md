---
title: specified
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'summary, clean-up MSDN import'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/HTMLElement
    href: /dom/HTMLElement
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/HTMLElement/specified

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Property of [dom/HTMLElement](/dom/HTMLElement)[dom/HTMLElement](/dom/HTMLElement)

## Syntax

``` js
var result = element.specified;
element.specified = value;
```

## Examples

The following code example uses the **specified** property to determine the attributes that are set for an object. The function checks each attribute and lists all of the attributes of the object and their values.

``` html
<script>
function fnFindSpecified(){
   var oAttributes=oList.attributes;
   alert(oAttributes(0).nodeName);
   for(var i=0;i<oAttributes.length;i++){
      var oNode=document.createElement("LI");
      var oNodeValue=document.createTextNode(i + " "
                     + oAttributes(i).nodeName + " = "
                     + oAttributes(i).nodeValue);
      oList.appendChild(oNode);
      oNode.appendChild(oNodeValue);
      if(oAttributes(i).nodeValue!=null){
         alert(oAttributes(i).nodeName
         + " specified: " + oAttributes(i).specified);
      }
   }
}
</script>
<ul id="oList" onclick= "fnFindSpecified()">
<li>Click to Find Specified Attributes</li>
</ul>
```

## Notes

### Remarks

An attribute value is specified if it is assigned through HTML or script. Windows Internet Explorer 9. When webpages are displayed in IE9 Standards mode, the [**attributes**](/dom/Node/attributes) collection does not contain attributes that are not specifically created (unlike previous Windows Internet Explorer versions). As a result, the **specified** property returns `true` for every item in the **attributes** collection.

### Syntax

### Standards information

-   [Document Object Model (DOM) Level 1 Specification](http://go.microsoft.com/fwlink/p/?linkid=161725), Section 1.2
