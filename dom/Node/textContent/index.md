---
title: textContent
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Sets or retrieves the text content of a node and any child nodes.'
uri: dom/Node/textContent

---
# textContent

## Summary

Sets or retrieves the text content of a node and any child nodes.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Node](/dom/Node)</span></span>

## Syntax

``` {.js}
var textContent = node.textContent;
node.textContent = newText;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

The text content of a node and its child nodes, if any.

## Examples

    // Given the following HTML fragment:
    //   This is some text
    // Get the text content:
    var text = document.getElementById("divA").textContent;
    //

The following example displays the textContent property of a \<script\> tag.

    <!DOCTYPE html>
    <html><head>
    <meta http-equiv="Content-Type" content="text/html; charset=utf-8">
    <script id="scrtest" type="text/javascript">
    function gettextContent(el){
    alert(el.textContent);
    }
    </script>
    <title>textContent example</title>
    </head>

    <body>
    <script type="text/javascript">
    gettextContent(document.getElementById('scrtest'));
    </script>



    </body></html>

## Notes

textContent returns null if the element is a document, a document type, or a notation. To grab all of the text and CDATA data for the whole document, one could use document.documentElement.textContent.

If the node is a CDATA section, a comment, a processing instruction, or a text node, textContent returns the text inside this node (the nodeValue).

For other node types, textContent returns the concatenation of the textContent attribute value of every child node, excluding comments and processing instruction nodes. This is an empty string if the node has no children.

Setting this property on a node removes all of its children and replaces them with a single text node with the given value.

## Related specifications

Specification
:   Status
[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Node.textContent](https://developer.mozilla.org/en-US/docs/Web/API/Node.textContent) Article]

Portions of this content come from the Microsoft Developer Network: [[textContent Property](http://msdn.microsoft.com/en-us/library/ie/ff974773(v=vs.85).aspx) Article]

