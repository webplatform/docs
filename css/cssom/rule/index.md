---
title: rule
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Double check correct printing of tokens, needs spec reference, standardization status'
readiness: 'In Progress'
summary: 'The rule object defines a set of Cascading Style Sheet (CSS) attributes applied to a set of HTML elements.'
tags:
  - API
  - Objects
  - DOM
uri: css/cssom/rule

---
## Summary

The rule object defines a set of Cascading Style Sheet (CSS) attributes applied to a set of HTML elements.

## Properties

API Name
:   Summary

[selectorText](/css/cssom/rule/selectorText)
:

## Methods

*No methods.*

## Events

*No events.*

## Examples

This example uses a **rule** object consisting of the selector **H1** to define a single rule that changes the H1 headings in a document to red.

``` html
<STYLE>
    H1 { color: red }
</STYLE>
```

If the style sheet containing the preceding rule is the first style sheet in the document, the following code returns the **rule** object associated with the rule.

``` js
oRule=document.styleSheets(0).rules(0)
```

## Notes

### Remarks

The **rule** object defines a set of Cascading Style Sheets (CSS) attributes applied to a set of HTML elements. For example, a rule consisting of the selector **H1** and the declaration [**font-family**](/css/properties/font-family):Arial defines all **H1** elements to render in the Arial font. This object is available in script as of Microsoft Internet Explorer 5.

## See also

### Related pages

-   `rules`
