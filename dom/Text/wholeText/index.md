---
title: wholeText
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Retrieves the immediate text child nodes of the parent node, that are adjacent to the text node.'
uri: dom/Text/wholeText

---
# wholeText

## Summary

Retrieves the immediate text child nodes of the parent node, that are adjacent to the text node.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Text](/dom/Text)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var text = textNode.wholeText;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

The text of the node and its adjacent text nodes.

## Examples

``` {.html}
<body>
<p id="p">this is a text node that also has <strong id="s">strong</strong> elements.</p>
<script type="text/javascript">
alert(document.getElementById('p').firstChild.wholeText);
// displays 'this is a text node that also has' in an alert box.
</script>
</body>
```

## Related specifications

Specification
:   Status
[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Text.wholeText](https://developer.mozilla.org/en-US/docs/Web/API/Text.wholeText) Article]

Portions of this content come from the Microsoft Developer Network: [[wholeText Property](http://msdn.microsoft.com/en-us/library/ie/ff974769(v=vs.85).aspx) Article]

