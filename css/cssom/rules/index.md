---
title: 'rules'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/rules_1.htm'
notes:
  - 'Needs spec reference, standardization status'
readiness: 'Almost Ready'
summary: 'The collection of rules in a stylesheet.'
tags:
  - API
  - Objects
  - DOM
uri: css/cssom/rules

---
## Summary

The collection of rules in a stylesheet.

## Properties

API Name
:   Summary

[item](/css/cssom/rules/item)
:

## Methods

*No methods.*

## Events

*No events.*

## Examples

This example shows how to use the **rules** collection to identify the color specified in style sheet rules.

``` js
<HTML>
<HEAD>
<SCRIPT>
function ruleColor(ruleIndex) {
    alert("The color of rule " + ruleIndex + " is " +
        document.styleSheets[0].rules.item(ruleIndex).style.color + ".");
}
</SCRIPT>
<STYLE>
.rule0 {color:"red"}
.rule1 {color:"blue"}
</STYLE>
</HEAD>
<BODY>
<P class="rule0" id="oRule0Span">
    Rule 0 is applied to this line.
</P>
<P class="rule1" id="oRule1Span">
    Rule 1 is applied to this line.
</P>
<BUTTON onclick="ruleColor(0)">Color of Rule 0</BUTTON>
<BUTTON onclick="ruleColor(1)">Color of Rule 1</BUTTON>
</BODY>
</HTML>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/rules_1.htm)

## Notes

### Remarks

This collection is always accessible, even if the style sheet is not enabled. Rules are added to the **rules** collection with the [**addRule**](/css/cssom/methods/addRule) method on the individual style sheet. A rule that is added to a [**disabled**](/html/attributes/disabled) style sheet does not apply to the document unless the style sheet is enabled. Rules are deleted with the [**removeRule**](/css/cssom/methods/removeRule) method. The rules in this collection are in the source order of the document. As rules are added or deleted through the Cascading Style Sheets (CSS) Object Model, a rule's absolute position in the **rules** collection might change, but its position relative to other rules remains the same. When you add rules without specifying an index, the rule gets added to the document last. If you specify an index, however, the rule is inserted before the rule currently in that ordinal position in the collection. If the specified index is greater than the number of rules in the collection, the rule is added to the end.
