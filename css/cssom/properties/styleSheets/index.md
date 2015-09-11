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
## <span>Summary</span>

Get a list of Style sheets applied to the current document as an ordered collection.

Property of [css/cssom/properties](/css/cssom/properties)[css/cssom/properties](/css/cssom/properties)

## <span>Syntax</span>

``` js
var result = element.styleSheets;
element.styleSheets = value;
```

## <span>Return Value</span>

Returns an object of type StyleSheetListStyleSheetList

Get a list of CSS Style Sheets assigned to the current document.

## <span>Notes</span>

### <span>Remarks</span>

Style sheets that are imported using the [**@import**](/css/atrules/@import) rule and are contained within the **style** object are available through the [**imports**](/css/cssom/imports) collection.

## <span>Related specifications</span>

[CSS Object Model (CSSOM), Section 6.2.3 Extensions to the Document Interface](http://www.w3.org/TR/cssom/)
:   W3C Working Draft

## <span>See also</span>

### <span>Other articles</span>

### <span>Related pages</span>

-   `link`
-   `style`
-   `CSSImportRule`
