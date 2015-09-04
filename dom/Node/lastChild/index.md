---
title: lastChild
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Gets a reference to the last child in the childNodes collection of an object. '
uri: dom/Node/lastChild

---
# lastChild

## Summary

Gets a reference to the last child in the childNodes collection of an object.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Node](/dom/Node)</span></span>

## Syntax

``` {.js}
var result = element.lastChild;
element.lastChild = value;
```

## Examples

The following code example implements the **lastChild** property to obtain a reference to the last child element of an object.

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

## Usage

     Used to remove and append nodes to user lists and tables.

### Syntax

var last\_child = element.lastChild

### Standards information

-   [Document Object Model (DOM) Level 1 Specification](http://go.microsoft.com/fwlink/p/?linkid=161725), Section 1.2

## Related specifications

Specification
:   Status
[DOM Level 2 Core](http://www.w3.org/TR/2000/REC-DOM-Level-2-Core-20001113/core.html#ID-61AD09FB)
:   Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Node.lastChild](https://developer.mozilla.org/en-US/docs/Web/API/Node.lastChild) Article]

Portions of this content come from the Microsoft Developer Network: [[lastChild Property](http://msdn.microsoft.com/en-us/library/ie/ms533943(v=vs.85).aspx) Article]

