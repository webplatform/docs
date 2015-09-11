---
title: lastChild
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Node.lastChild](https://developer.mozilla.org/en-US/docs/Web/API/Node.lastChild) Article]'
  - 'Microsoft Developer Network: [[lastChild Property](http://msdn.microsoft.com/en-us/library/ie/ms533943(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Node
    href: /dom/Node
standardization_status: 'W3C Recommendation'
summary: 'Gets a reference to the last child in the childNodes collection of an object. '
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/Node/lastChild

---
## <span>Summary</span>

Gets a reference to the last child in the childNodes collection of an object.

Property of [dom/Node](/dom/Node)[dom/Node](/dom/Node)

## <span>Syntax</span>

``` js
var result = element.lastChild;
element.lastChild = value;
```

## <span>Examples</span>

The following code example implements the **lastChild** property to obtain a reference to the last child element of an object.

``` html
<body>
<ul id = "oList">
<li>List Item 1</li>
<li>List Item 2</li>
<li>List Item 3</li>
</ul>
<script type="text/javascript">
var olastChild = oList.lastChild;
</script>
<body>
```

## <span>Usage</span>

     Used to remove and append nodes to user lists and tables.

### <span>Syntax</span>

var last\_child = element.lastChild

### <span>Standards information</span>

-   [Document Object Model (DOM) Level 1 Specification](http://go.microsoft.com/fwlink/p/?linkid=161725), Section 1.2

## <span>Related specifications</span>

[DOM Level 2 Core](http://www.w3.org/TR/2000/REC-DOM-Level-2-Core-20001113/core.html#ID-61AD09FB)
:   Recommendation
