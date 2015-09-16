---
title: 'wholeText'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Text.wholeText](https://developer.mozilla.org/en-US/docs/Web/API/Text.wholeText) Article]'
  - 'Microsoft Developer Network: [[wholeText Property](http://msdn.microsoft.com/en-us/library/ie/ff974769(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Text
    href: /dom/Text
  return:
    predicate: 'Returns an object of type '
    value: String
    href: /dom/Text
standardization_status: 'W3C Recommendation'
summary: 'Retrieves the immediate text child nodes of the parent node, that are adjacent to the text node.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/Text/wholeText

---
## Summary

Retrieves the immediate text child nodes of the parent node, that are adjacent to the text node.

Property of [dom/Text](/dom/Text)[dom/Text](/dom/Text)

## Syntax

**Note**: This property is read-only.

``` js
var text = textNode.wholeText;
```

## Return Value

Returns an object of type StringString

The text of the node and its adjacent text nodes.

## Examples

``` html
<body>
<p id="p">this is a text node that also has <strong id="s">strong</strong> elements.</p>
<script type="text/javascript">
alert(document.getElementById('p').firstChild.wholeText);
// displays 'this is a text node that also has' in an alert box.
</script>
</body>
```

## Related specifications

[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation
