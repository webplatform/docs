---
title: textContent
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Node.textContent](https://developer.mozilla.org/en-US/docs/Web/API/Node.textContent) Article]'
  - 'Microsoft Developer Network: [[textContent Property](http://msdn.microsoft.com/en-us/library/ie/ff974773(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Node
    href: /dom/Node
  return:
    predicate: 'Returns an object of type '
    value: String
    href: /dom/Node
standardization_status: 'W3C Recommendation'
summary: 'Sets or retrieves the text content of a node and any child nodes.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/Node/textContent

---
## <span>Summary</span>

Sets or retrieves the text content of a node and any child nodes.

Property of [dom/Node](/dom/Node)[dom/Node](/dom/Node)

## <span>Syntax</span>

``` js
var textContent = node.textContent;
node.textContent = newText;
```

## <span>Return Value</span>

Returns an object of type StringString

The text content of a node and its child nodes, if any.

## <span>Examples</span>

``` html
// Given the following HTML fragment:
//   <div id="divA">This is <span>some</span> text</div>

// Get the text content:
var text = document.getElementById("divA").textContent;
//
```

The following example displays the textContent property of a \<script\> tag.

``` html
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
```

## <span>Notes</span>

textContent returns null if the element is a document, a document type, or a notation. To grab all of the text and CDATA data for the whole document, one could use document.documentElement.textContent.

If the node is a CDATA section, a comment, a processing instruction, or a text node, textContent returns the text inside this node (the nodeValue).

For other node types, textContent returns the concatenation of the textContent attribute value of every child node, excluding comments and processing instruction nodes. This is an empty string if the node has no children.

Setting this property on a node removes all of its children and replaces them with a single text node with the given value.

## <span>Related specifications</span>

[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation
