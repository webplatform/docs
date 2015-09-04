---
title: styleSheets
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Not Ready'
standardization_status: 'W3C Working Draft'
notes:
  - 'Cannot finish, Spec is still at Draft level anyway.'
summary: 'Get a list of Style sheets applied to the current document as an ordered collection.'
uri: css/cssom/properties/styleSheets

---
# styleSheets

## Summary

Get a list of Style sheets applied to the current document as an ordered collection.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[css/cssom/properties](/css/cssom/properties)</span></span>

## Syntax

``` {.js}
var result = element.styleSheets;
element.styleSheets = value;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">StyleSheetList</span></span>

Get a list of CSS Style Sheets assigned to the current document.

## Notes

### Remarks

Style sheets that are imported using the [**@import**](/css/atrules/@import) rule and are contained within the **style** object are available through the [**imports**](/css/cssom/imports) collection.

## Related specifications

Specification
:   Status
[CSS Object Model (CSSOM), Section 6.2.3 Extensions to the Document Interface](http://www.w3.org/TR/cssom/)
:   W3C Working Draft

## See also

### Other articles

### Related pages

-   `link`
-   `style`
-   `CSSImportRule`

