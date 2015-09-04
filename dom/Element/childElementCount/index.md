---
title: childElementCount
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Almost Ready'
standardization_status: 'W3C Recommendation'
notes:
  - 'Needs compat table'
summary: 'Returns the number of direct children of this node that are elements.  Read-only.'
uri: dom/Element/childElementCount

---
# childElementCount

## Summary

Returns the number of direct children of this node that are elements. Read-only.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Element](/dom/Element)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = element.childElementCount;
```

## Examples

This example shows how to use **childElementCount** to get the number of *immediate* children of a div tag. Descendent children of the the div tag "divWithChildren" are ignored.

    <!DOCTYPE html>
    <html>
    <head>
            <title>childElementCount example</title>
        <script>
            function GetCount () {
                var testArea = document.getElementById ("testArea");
                var childCount = 0;
                    childCount = testArea.childElementCount;
                alert ("The number of child elements is " + childCount);
            }
        </script>
    </head>
    <body>
        <div id="testArea" >
        <p>This is the test area, which contains several children.</p>
            <div id="divWithChildren">
                <div>a descendant child of a div</div>
                <div>also a descendent child of a div</div>
            </div>
            <p>A paragraph tag to consider.</p>
            <input type="text" size="80" value="And a text box as well"/>
        </div>
        <p><input type="button" value="Get the number child elements in our test" name="abutton"  onclick="GetCount ();" /> </p>

    </body>
    </html>

## Notes

### Remarks

The **childElementCount** property only returns immediate children of the current node. It does not count descendent children of the immediate children.

### Syntax

### Standards information

-   [Element Traversal Specification](http://go.microsoft.com/fwlink/p/?linkid=182722), Section 2.5

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

