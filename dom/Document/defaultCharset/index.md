---
title: defaultCharset
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs a note that this is not a W3C standard and does not work in most browsers, also needs compat table'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Document
    href: /dom/Document
  return:
    predicate: 'Returns an object of type '
    value: String
    href: /dom/Document
standardization_status: Non-Standard
summary: 'Gets the default character set from the current regional language settings.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/Document/defaultCharset

---
## <span>Summary</span>

Gets the default character set from the current regional language settings.

Property of [dom/Document](/dom/Document)[dom/Document](/dom/Document)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var defaultCharacterSet = document.defaultCharset;
```

## <span>Return Value</span>

Returns an object of type StringString

The name of the default character set of the user.

## <span>Examples</span>

``` js
//displays the document's default character encoding string
function showDefCharSet() {
    alert(document.defaultCharset);
}
```

## <span>Notes</span>

The value depends on the current regional language settings. For typical settings in North America, the value is `windows-1252`.