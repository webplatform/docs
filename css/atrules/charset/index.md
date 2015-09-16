---
title: @charset
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Specifies the character encoding of the style sheet.'
tags:
  - CSS
  - At
  - Rules
uri: css/atrules/@charset

---
## Summary

Specifies the character encoding of the style sheet.

## Examples

Set the character encoding of the style sheet to Unicode UTF-8 (recommended)

``` css
@charset "UTF-8";
```

Set the character encoding of the style sheet to Cyrillic (Windows 1251)

``` css
@charset "Windows-1251";
```

## Notes

### Remarks

You can use only one **@charset** rule in an external style sheet. The rule must appear at the top of the file, cannot be preceded by any characters, and cannot be included in an embedded style sheet.

The rule has no default value.

### Syntax

`@charset CharSet-Description`

### Parameters

*CharSet-Description*
:   **String** that specifies the name of the character encoding.

### Standards information

-   [CSS 2.1](http://go.microsoft.com/fwlink/p/?linkid=203757), Section 4.4

## Related specifications

[Cascading Style Sheets Level 2 Revision 1 (CSS 2.1)](http://www.w3.org/TR/CSS2/)
:   Recommendation

## See also

### Related articles

#### Syntax

-   **@charset**

-   [@font-face](/css/atrules/@font-face)

-   [@import](/css/atrules/@import)

-   [@keyframes](/css/atrules/@keyframes)

-   [@namespace](/css/atrules/@namespace)

-   [@page](/css/atrules/@page)

-   [@supports](/css/atrules/@supports)

-   [CSS reference](/css/reference)

-   [Alphabetical list of CSS reference](/css/reference/alphabetical)

-   [!important](/css/syntax/!important)
