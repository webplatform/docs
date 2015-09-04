---
title: cssText
tags:
  - API
  - Object
  - Properties
  - CSS
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Gets or sets the textual representation of a CSS style declaration.'
uri: css/cssom/CSSStyleDeclaration/cssText

---
# cssText

## Summary

Gets or sets the textual representation of a CSS style declaration.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration](/css/cssom/CSSStyleDeclaration/CSSStyleDeclaration)</span></span>

## Syntax

``` {.js}
var declarationText = declaration.cssText;
declaration.cssText = declarationText;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

The textual representation of the CSS style declaration.

## Examples

``` {.css}
<style>
body { background-color: darkblue; }
</style>
<script>
  var stylesheet = document.styleSheets[0];
  alert(stylesheet.cssRules[0].cssText);
  // returns "body { background-color: darkblue; }"
</script>
```

## Notes

This property reflects the current state of the declaration and not its initial value.

## Related specifications

Specification
:   Status
[DOM Level 2 Style](http://www.w3.org/TR/DOM-Level-2-Style/css.html)
:   Recommendation

