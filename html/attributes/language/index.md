---
title: language
tags:
  - Markup
  - Attributes
  - HTML
readiness: 'Not Ready'
standardization_status: Deprecated
notes:
  - 'Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info'
summary: 'Use the type attribute instead. Specifies the language of the script to be evaluated. May be omitted when using ECMAScript (also known as JavaScript).'
uri: html/attributes/language

---
# language

## Summary

Use the type attribute instead. Specifies the language of the script to be evaluated. May be omitted when using ECMAScript (also known as JavaScript).

Applies to
:   dom/HTMLScriptElement

**Needs Examples**: This section should include examples.

## Usage

     Use this attribute only when you want the browser to evaluate the script in a language or a version of the language other than the default. If the browser does not support the specified language or version of the language, the script will not be evaluated.

## Notes

-   See the [lang](/html/attributes/lang) attribute if you want to declare the natural language of your content, eg. French, etc.
-   When a [type](/html/attributes/type) attribute is also specified, it takes precedence over this attribute and this attribute will be ignored.

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

