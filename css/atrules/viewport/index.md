---
title: @viewport
tags:
  - CSS
  - At
  - Rules
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Specifies the size, zoom factor, and orientation of the viewport.'
uri: css/atrules/@viewport

---
# @viewport

## Summary

Specifies the size, zoom factor, and orientation of the viewport.

## Examples

``` {.css}
@media screen and (max-width:400px) {
    @-ms-viewport{
        width:320px;
        /* the viewport for small devices is set to 320px  */
    }
    @-o-viewport {
        width: device-width;
    }
    @viewport {
        width: device-width;
    }
}
```

## Notes

### Remarks

You can use the **@viewport** rule in tandem with media queries to help optimize your layout. Typically, you nest the **@viewport** rule inside the media query, as shown in the following pseudocode snippet: `@media [media query logic here] { @viewport { [viewport properties here] } [CSS for this layout combination here] }`

### Syntax

`@viewport { viewport-properties }`

### Parameters

*viewport-properties*
:   One or more property declarations, each with a trailing semicolon. Only the following viewport properties are supported.

<dl>
<dt>
Value

</dt>
<dd>
Meaning

</dd>
<dt>
<dl>
<dt>
**width**

</dt>
</dl>
</dt>
<dd>
Indicates the preferred viewport width used in determining the size of the initial containing block. Can be one of the following values:

 **auto**
:   The value is calculated based on the display device's normal mode of operation.
 **device-width**
:   The width of the screen in CSS pixels at a zoom factor of 100%.
 **device-height**
:   The height of the screen in CSS pixels at a zoom factor of 100%.
 **length**
:   A positive absolute or relative length.
 **percentage**
:   A positive percentage value relative to the width or height of the initial viewport at a zoom factor of 100%, for horizontal and vertical lengths respectively.

</dd>
<dt>
<dl>
<dt>
**height**

</dt>
</dl>
</dt>
<dd>
Indicates the preferred viewport height used in determining the size of the initial containing block. See **width** for a list of possible values.

</dd>
</dl>
## Related specifications

Specification
:   Status
[CSS Device Adaptation](http://www.w3.org/TR/css-device-adapt/#the-viewport-rule)
:   Working Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

**Content Incomplete**: Some of this page's content is incomplete.

