---
title: nodeName
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Gets the name of a particular type of node.'
uri: dom/Node/nodeName

---
# nodeName

## Summary

Gets the name of a particular type of node.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Node](/dom/Node)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var nodeName = node.nodeName;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

The uppercase name of the node if Content type is text/html, else the lowercase name of the node if Content type is xhtml or any other xml content type.

## Examples

The following code example uses the **nodeName** property to obtain the name of an element.

``` {.html}
<body>
 <ul id="oList">
  <li>List Item 1</li>
  <li>List Item 2</li>
  <li>List Item 3</li>
 </ul>
<script type="text/javascript">
// returns the element name 'LI' of the list item labeled 'List Item 2'
var sName = document.getElementById("oList").childNodes(1).nodeName;
</script>

</body>
```

## Notes

The html spec allows tag names of either case, upper or lower-case. The xhtml spec requires tag names in lower-case only. For interoperability between html and xhtml, and for markup re-use in html and xhtml documents user lower-case tag names in your source markup.

Using lower-case tag names in your source markup also require less keystrokes!

Read more details on [nodeName case sensitivity in different browsers.](http://ejohn.org/blog/nodename-case-sensitivity/)

## Related specifications

Specification
:   Status
[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Node.nodeName](https://developer.mozilla.org/en-US/docs/Web/API/Node.nodeName) Article]

Portions of this content come from the Microsoft Developer Network: [[nodeName Property](http://msdn.microsoft.com/en-us/library/ie/ms534190(v=vs.85).aspx) Article]

