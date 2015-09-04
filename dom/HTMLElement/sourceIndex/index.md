---
title: sourceIndex
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Not Ready'
notes:
  - 'summary, clean-up MSDN import'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/sourceIndex.htm'
uri: dom/HTMLElement/sourceIndex

---
# sourceIndex

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/HTMLElement](/dom/HTMLElement)</span></span>

## Syntax

``` {.js}
var result = element.sourceIndex;
element.sourceIndex = value;
```

## Examples

This example uses the **sourceIndex** property to identify the previous and next elements in the **all** collection (deprecated).

    <SCRIPT>
    function fnHandler(){
       // Retrieve the element that fired the event.
       var oElement=event.srcElement;
       var iIndex=oElement.sourceIndex;
       var sTagName=oElement.tagName;
       if(sTagName=="!"){
          sTagName="COMMENT";
       }
       oVal1.innerText=iIndex;
       oVal2.innerText=sTagName;
       if(iIndex-1>0){
          sTagName=document.all[iIndex-1].tagName;
          if(sTagName=="!"){
             sTagName="COMMENT";
          }
          oVal3.innerText=sTagName;
       }
       else{
          oVal3.innerText="Cannot read.";
       }
       if(iIndex+1<document.all.length){
          sTagName=document.all[iIndex+1].tagName;
          if(sTagName=="!"){
             sTagName="COMMENT";
          }
          oVal4.innerText=sTagName;
       }
       else{
          oVal4.innerText="Cannot read.";
       }
    }
    </SCRIPT>

    <BODY onmousemove="fnHandler()">
    <TABLE>
    <TR><TD>Source Index:</TD><TD ID=oVal1></TD></TR>
    <TR><TD>Object Name:</TD><TD ID=oVal2></TD></TR>
    <TR><TD>Previous Object:</TD><TD ID=oVal3></TD></TR>
    <TR><TD>Next Object:</TD><TD ID=oVal4></TD></TR>
    </TABLE>
    </BODY>

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/sourceIndex.htm)

### Syntax

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

