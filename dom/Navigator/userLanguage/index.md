---
title: userLanguage
attributions:
  - 'Microsoft Developer Network: [[navigator.userLanguage](http://msdn.microsoft.com/en-us/library/ie/ms534713(v=vs.85).aspx) Article]'
code_samples:
  - 'http://result.dabblet.com/gist/b1e7c611e97594b60956/56337717d0b88e99b8944707d60bb7072b359788'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Navigator
    href: /dom/Navigator
  return:
    predicate: 'Returns an object of type '
    value: String
    href: /dom/Navigator
standardization_status: Non-Standard
summary: "Retrieves the operating system's natural language setting.\n"
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/Navigator/userLanguage

---
## Summary

Retrieves the operating system's natural language setting.

This property reflects the setting in the "Your locale (location)" box in the Regional Options of Control Panel—for example, "English (United States).

Property of [dom/Navigator](/dom/Navigator)[dom/Navigator](/dom/Navigator)

## Syntax

**Note**: This property is read-only.

``` js
var result = navigator.userLanguage;
```

## Return Value

Returns an object of type StringString

see [Language Codes](http://msdn.microsoft.com/en-us/library/ms533052(v=vs.85).aspx) for a full listing of possible values.

## Examples

This example enumerates the properties and methods of your web browsers 'navigator' object and displays the results on the screen.

the navigator.userLanguage may or may not be supported by your web browser.

``` html

```

[View live example](http://result.dabblet.com/gist/b1e7c611e97594b60956/56337717d0b88e99b8944707d60bb7072b359788)

## Usage

     Do not use as this property reflects the language preferences of the users' Operating system NOT their language preferences for web content.

## Notes

### Remarks

This property reflects the setting in the "Your locale (location)" box in the Regional Options of Control Panel—for example, "English (United States).

### Syntax

var result=navigator.userLanguage;
