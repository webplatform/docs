---
title: controlRange
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'In Progress'
notes:
  - 'summary, examples best practices, compatibility, standards, clean-up of MSDN sections'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/collections/controlrange.htm'
uri: dom/HTMLElement/controlRange

---
# controlRange

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/HTMLElement](/dom/HTMLElement)</span></span>

## Syntax

``` {.js}
var result = element.controlRange;
element.controlRange = value;
```

## Examples

This example demonstrates how to use the [**createRange**](/dom/Selection/createRange) method to retrieve the **controlRange** collection.

    ...
    function fnChangeFontFamily    (){
      if (document.selection.type == "Control"){
        var oControlRange = document.selection.createRange();
        for (i = 0; i < oControlRange.length; i++)
          if (oControlRange(i).tagName != "IMG")
           oControlRange(i).style.fontFamily=event.srcElement.style.fontFamily;
      }
    }
    ...
    <!-- Text Font-Family Controls  -->
    <SPAN  onclick="fnChangeFontFamily();">
        <DIV STYLE="height: 25px; cursor:hand; font-family:times;
            font-size:14pt; font-weight:normal; color:white">Times</DIV>
        <DIV STYLE="height: 25px; cursor:hand; font-family:arial;
            font-size:14pt; font-weight:normal; color:white">Arial</DIV>
        <DIV STYLE="height: 25px; cursor:hand; font-family:georgia;
            font-size:14pt; font-weight:normal; color:white">Georgia</DIV>
        <DIV STYLE="height: 25px; cursor:hand; font-family:verdana;
            font-size:14pt; font-weight:normal; color:white">Verdana</DIV>
    </SPAN><BR/>
    ...

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/collections/controlrange.htm)

## Notes

### Remarks

Instead of using the collection's [**item**](/dom/HTMLCollection/item) method, you can use an index to directly access an element in the collection. For example, the element returned from the collection represented by `oColl(0)` is the same as the element returned by `oColl.item(0)`. The **controlRange** collection is available as of Microsoft Internet Explorer 5.

### Syntax

### Standards information

There are no standards that apply here.

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

