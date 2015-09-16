---
title: styleSheets
notes:
  - 'Cannot finish, Spec is still at Draft level anyway.'
readiness: 'Not Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: css/cssom/properties
    href: /css/cssom/properties
  return:
    predicate: 'Returns an object of type '
    value: StyleSheetList
    href: /css/cssom/properties
standardization_status: 'W3C Working Draft'
summary: 'Get a list of Style sheets applied to the current document as an ordered collection.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: css/cssom/properties/styleSheets

---
## Summary

Get a list of Style sheets applied to the current document as an ordered collection.

Property of [css/cssom/properties](/css/cssom/properties)[css/cssom/properties](/css/cssom/properties)

## Syntax

``` js
var result = element.styleSheets;
element.styleSheets = value;
```

## Return Value

Returns an object of type StyleSheetListStyleSheetList

Get a list of CSS Style Sheets assigned to the current document.

## Notes

### Remarks

Style sheets that are imported using the [**@import**](/css/atrules/@import) rule and are contained within the **style** object are available through the [**imports**](/css/cssom/imports) collection.

## Related specifications

[CSS Object Model (CSSOM), Section 6.2.3 Extensions to the Document Interface](http://www.w3.org/TR/cssom/)
:   W3C Working Draft

## See also

### Other articles

### Related pages

-   `link`
-   `style`
-   `CSSImportRule`
