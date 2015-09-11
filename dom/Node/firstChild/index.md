---
title: firstChild
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Node.firstChild](https://developer.mozilla.org/en-US/docs/Web/API/Node.firstChild) Article]'
  - 'Microsoft Developer Network: [[firstChild Property](http://msdn.microsoft.com/en-us/library/ie/ms533755(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Node
    href: /dom/Node
  return:
    predicate: 'Returns an object of type '
    value: Element
    href: /dom/Node
summary: "Gets a reference to the first child node in the childNodes collection of the object.\n"
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/Node/firstChild

---
## <span>Summary</span>

Gets a reference to the first child node in the childNodes collection of the object.

If the node is childless, null is returned.

Property of [dom/Node](/dom/Node)[dom/Node](/dom/Node)

## <span>Syntax</span>

``` js
var result = element.firstChild;
element.firstChild = value;
```

## <span>Return Value</span>

Returns an object of type ElementElement

## <span>Examples</span>

The following code example implements the **firstChild** attribute to get the first child element of an object.

``` html
<body>
<ul id ="oList">
<li>List Item 1</li>
<li>List Item 2</li>
<li>List Item 3</li>
</ul>
<script type="text/javascript">
var oFirstChild = oList.firstChild;
</script>
</body>
```

The following example shows how the firstChild method will include white space nodes \#text.

``` html
<p id="para-01">
  <span>First span</span>
</p>
<p id="p2"><span>first span, no whitespace</span></p>
<script type="text/javascript">
  var p01 = document.getElementById('para-01');
  alert(p01.firstChild.nodeName);// #text
  var p2=document.getElementById('p2');
  alert(p2.firstChild.nodeName);// SPAN
</script>
```

### <span>Syntax</span>

### <span>Standards information</span>

-   [Document Object Model (DOM) Level 1 Specification](http://go.microsoft.com/fwlink/p/?linkid=161725), Section 1.2
