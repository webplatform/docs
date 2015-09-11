---
title: cssText
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: css/cssom/CSSStyleDeclaration/CSSStyleDeclaration
    href: /css/cssom/CSSStyleDeclaration/CSSStyleDeclaration
  return:
    predicate: 'Returns an object of type '
    value: String
    href: /css/cssom/CSSStyleDeclaration/CSSStyleDeclaration
standardization_status: 'W3C Recommendation'
summary: 'Gets or sets the textual representation of a CSS style declaration.'
tags:
  - API
  - Object
  - Properties
  - CSS
  - DOM
uri: css/cssom/CSSStyleDeclaration/cssText

---
## <span>Summary</span>

Gets or sets the textual representation of a CSS style declaration.

Property of [css/cssom/CSSStyleDeclaration/CSSStyleDeclaration](/css/cssom/CSSStyleDeclaration/CSSStyleDeclaration)[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration](/css/cssom/CSSStyleDeclaration/CSSStyleDeclaration)

## <span>Syntax</span>

``` js
var declarationText = declaration.cssText;
declaration.cssText = declarationText;
```

## <span>Return Value</span>

Returns an object of type StringString

The textual representation of the CSS style declaration.

## <span>Examples</span>

``` css
<style>
body { background-color: darkblue; }
</style>
<script>
  var stylesheet = document.styleSheets[0];
  alert(stylesheet.cssRules[0].cssText);
  // returns "body { background-color: darkblue; }"
</script>
```

## <span>Notes</span>

This property reflects the current state of the declaration and not its initial value.

## <span>Related specifications</span>

[DOM Level 2 Style](http://www.w3.org/TR/DOM-Level-2-Style/css.html)
:   Recommendation
