---
title: addRule
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs summary, spec reference, standardization status'
readiness: 'In Progress'
relationships:
  method_of:
    predicate: 'Method of '
    value: css/cssom/methods
    href: /css/cssom/methods
  return_type:
    predicate: 'Returns an object of type  '
    value: ''
    href: /css/cssom/methods
tags:
  - API
  - Object
  - Methods
  - DOM
uri: css/cssom/methods/addRule

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Method of [css/cssom/methods](/css/cssom/methods)[css/cssom/methods](/css/cssom/methods)

## <span>Syntax</span>

``` js
var object = object.addRule(Selector, Style, Index);
```

## <span>Parameters</span>

### <span>Selector</span>

 Data-type
:   String

**String** that specifies the selector for the new rule. Single contextual selectors are valid. For example, "**div** **p** **b**" is a valid contextual selector.

### <span>Style</span>

 Data-type
:   String

**String** that specifies the style assignments for this style rule. This style takes the same form as an inline style specification. For example, "`color:blue`" is a valid style parameter.

### <span>Index</span>

 Data-type
:   Number

**Integer** that specifies the zero-based position in the **rules** collection where the new style rule should be placed. Default is **-1**, which specifies that the rule is added to the end of the collection.

## <span>Return Value</span>

Returns an object of type<span></span>

Reserved. Always returns -1.

## <span>Examples</span>

This example uses the **addRule** method to add a rule that sets all bold text appearing in a DIV to the color blue.

``` html
<STYLE>
</STYLE>
<DIV>
Internet Explorer makes <B>HTML</B> dynamic.
</DIV>
<SCRIPT>
   var new_rule;
   new_rule = document.styleSheets[0].addRule("DIV B", "color:blue", 0);
</SCRIPT>
```

## <span>Notes</span>

### <span>Remarks</span>

You can add up to 4095 style rules with the **addRule** method. After that, the method returns an "Invalid Argument" exception. You can apply rules to a disabled [**styleSheet**](/css/cssom/styleSheet), but they do not apply to the document until you enable the **styleSheet**.

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `IHTMLStyleSheet`
-   `styleSheet`
-   `Reference`
-   `removeRule`
-   `rules`
-   `styleSheets`
