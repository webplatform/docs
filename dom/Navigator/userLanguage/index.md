---
title: userLanguage
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Ready to Use'
standardization_status: Non-Standard
summary: "Retrieves the operating system's natural language setting.\n"
code_samples:
  - 'http://result.dabblet.com/gist/b1e7c611e97594b60956/56337717d0b88e99b8944707d60bb7072b359788'
uri: dom/Navigator/userLanguage

---
# userLanguage

## Summary

Retrieves the operating system's natural language setting.

This property reflects the setting in the "Your locale (location)" box in the Regional Options of Control Panel—for example, "English (United States).

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Navigator](/dom/Navigator)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = navigator.userLanguage;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

see [Language Codes](http://msdn.microsoft.com/en-us/library/ms533052(v=vs.85).aspx) for a full listing of possible values.

## Examples

This example enumerates the properties and methods of your web browsers 'navigator' object and displays the results on the screen.

the navigator.userLanguage may or may not be supported by your web browser.

[View live example](http://result.dabblet.com/gist/b1e7c611e97594b60956/56337717d0b88e99b8944707d60bb7072b359788)

## Usage

     Do not use as this property reflects the language preferences of the users' Operating system NOT their language preferences for web content.

## Notes

### Remarks

This property reflects the setting in the "Your locale (location)" box in the Regional Options of Control Panel—for example, "English (United States).

### Syntax

var result=navigator.userLanguage;

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[navigator.userLanguage](http://msdn.microsoft.com/en-us/library/ie/ms534713(v=vs.85).aspx) Article]

