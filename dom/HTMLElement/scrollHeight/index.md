---
title: 'scrollHeight'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/scrollHeight.htm'
notes:
  - 'summary, clean-up of MSDN import'
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
uri: dom/HTMLElement/scrollHeight

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Property of [dom/HTMLElement](/dom/HTMLElement)[dom/HTMLElement](/dom/HTMLElement)

## Syntax

``` js
var result = element.scrollHeight;
element.scrollHeight = value;
```

## Examples

This example uses the **scrollHeight** property to retrieve the height of the viewable content.

``` html
<script type="text/javascript">
function fnCheckScroll(){
    var iNewHeight = oDiv.scrollHeight;
    alert("The value of the scrollHeight property is: "
        + iNewHeight + "px");
}
</script>
...
<div id="oDiv" style="overflow: scroll; height= 100px; width= 250px; text-align: left">
    ...
</div>
<button onclick="fnCheckScroll()">Check scrollHeight</button>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/scrollHeight.htm)

## Notes

### Remarks

The height is the distance between the top and bottom edges of the object's content. This property is read-only on HTML documents, and read-write on fixed regions. For more information about how to access the dimension and location of objects on the page through the Dynamic HTML (DHTML) Object Model, see Measuring Element Dimension and Location with CSSOM in Internet Explorer 9.

### Syntax
