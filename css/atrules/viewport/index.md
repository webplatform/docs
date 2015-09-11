---
title: @viewport
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Specifies the size, zoom factor, and orientation of the viewport.'
tags:
  - CSS
  - At
  - Rules
uri: css/atrules/@viewport

---
## <span>Summary</span>

Specifies the size, zoom factor, and orientation of the viewport.

## <span>Examples</span>

``` css
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

## <span>Notes</span>

### <span>Remarks</span>

You can use the **@viewport** rule in tandem with media queries to help optimize your layout. Typically, you nest the **@viewport** rule inside the media query, as shown in the following pseudocode snippet: `@media [media query logic here] { @viewport { [viewport properties here] } [CSS for this layout combination here] }`

### <span>Syntax</span>

`@viewport { viewport-properties }`

### <span>Parameters</span>

*viewport-properties*
:   One or more property declarations, each with a trailing semicolon. Only the following viewport properties are supported.

<table>
<col width="50%" />
<col width="50%" />
<thead>
<tr class="header">
<th align="left">Value</th>
<th align="left">Meaning</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><dl>
<dt>
<strong>width</strong>
</dt>
</dl></td>
<td align="left"><p>Indicates the preferred viewport width used in determining the size of the initial containing block. Can be one of the following values:</p>
<dl>
<dt> <strong>auto</strong></dt>
<dd>The value is calculated based on the display device's normal mode of operation.
</dd>
<dt> <strong>device-width</strong></dt>
<dd>The width of the screen in CSS pixels at a zoom factor of 100%.
</dd>
<dt> <strong>device-height</strong></dt>
<dd>The height of the screen in CSS pixels at a zoom factor of 100%.
</dd>
<dt> <strong>length</strong></dt>
<dd>A positive absolute or relative length.
</dd>
<dt> <strong>percentage</strong></dt>
<dd>A positive percentage value relative to the width or height of the initial viewport at a zoom factor of 100%, for horizontal and vertical lengths respectively.
</dd>
</dl></td>
</tr>
<tr class="even">
<td align="left"><dl>
<dt>
<strong>height</strong>
</dt>
</dl></td>
<td align="left">Indicates the preferred viewport height used in determining the size of the initial containing block. See <strong>width</strong> for a list of possible values.</td>
</tr>
</tbody>
</table>

## <span>Related specifications</span>

[CSS Device Adaptation](http://www.w3.org/TR/css-device-adapt/#the-viewport-rule)
:   Working Draft

**Content Incomplete**: Some of this page's content is incomplete.

