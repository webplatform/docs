---
title: scrollTop
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'In Progress'
notes:
  - 'summary, clean-up of MSDN import'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/scrollTop.htm'
uri: dom/HTMLElement/scrollTop

---
# scrollTop

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/HTMLElement](/dom/HTMLElement)</span></span>

## Syntax

``` {.js}
var result = element.scrollTop;
element.scrollTop = value;
```

## Examples

This example uses the **scrollTop** property to determine the amount scrolled by the object.

    <div id="oDiv" style="position: absolute;
        width: 200px;
        height: 100px;
        overflow: scroll"
        onclick="alert(this.scrollTop)">
        <span style="width: 250px">. . . </span>
    </div>

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/scrollTop.htm)

## Notes

### Remarks

This property's value equals the current vertical offset of the content within the scrollable range. Although you can set this property to any value, if you assign a value less than 0, the property is set to 0. If you assign a value greater than the maximum value, the property is set to the maximum value. You can set this property inline, but the results might be inconsistent while the document is loading. This property is always 0 for objects that do not have scroll bars. For these objects, setting the property has no effect. When a **marquee** object scrolls horizontally, its **scrollTop** property is set to 0, overriding any script setting. For more information about how to access the dimension and location of elements on the document through the Dynamic HTML (DHTML) Object Model, see Measuring Element Dimension and Location with CSSOM in Internet Explorer 9.

### Syntax

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

