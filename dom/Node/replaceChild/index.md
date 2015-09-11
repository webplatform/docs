---
title: replaceChild
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Node.replaceChild](https://developer.mozilla.org/en-US/docs/Web/API/Node.replaceChild) Article]'
  - 'Microsoft Developer Network: [[replaceChild Method](http://msdn.microsoft.com/en-us/library/ie/ms536716(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Node
    href: /dom/Node
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /dom/Node
standardization_status: 'W3C Recommendation'
summary: 'Replaces an existing child node with a new child node.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/Node/replaceChild

---
## <span>Summary</span>

Replaces an existing child node with a new child node.

Method of [dom/Node](/dom/Node)[dom/Node](/dom/Node)

## <span>Syntax</span>

``` js
var replacedNode = node.replaceChild(/* see parameter list */);
```

## <span>Parameters</span>

### <span>newChild</span>

 Data-type
:   DOM Node

 The new node to be inserted into the document.

### <span>oldChild</span>

 Data-type
:   DOM Node

 The existing node to be replaced.

## <span>Return Value</span>

Returns an object of type DOM NodeDOM Node

**IHTMLDOMNode**

Returns a reference to the object that is replaced.

## <span>Examples</span>

This example uses the **replaceChild** method to replace a bold element from a **div** with an italic element.

``` html
<!doctype html>
<head>
<script>
function replaceElement()
{
var Div1 = document.getElementById("Div1");
        //The first child of the div is the bold element.
    var oChild=Div1.children(0);
    var sInnerHTML = oChild.innerHTML;
    if (oChild.tagName=="B")
    {
        oNewChild=document.createElement("I");
        Div1.replaceChild(oNewChild, oChild);
        oNewChild.innerHTML=sInnerHTML
    }
    else
    {
        oNewChild=document.createElement("B");
        Div1.replaceChild(oNewChild, oChild);
        oNewChild.innerHTML=sInnerHTML
    }
}
</script>
</head>
<body>
<div id="Div1" onclick="replaceElement()">
Click anywhere in this sentence to toggle this <strong>word</strong>
between bold and italic.</div>
</body>
```

## <span>Notes</span>

The node to be replaced must be an immediate child of the parent object. The new node must be created using the [**createElement**](/dom/Document/createElement) method. This property is accessible at run time. If elements are removed at run time, before the closing tag is parsed, areas of the document might not render.

## <span>Related specifications</span>

[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation
