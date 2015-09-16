---
title: @font-face
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/CSS/@font-face)'
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/ms530757(v=vs.85).aspx)'
code_samples:
  - 'http://gist.github.com/5481068'
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'The @font-face CSS at-rule allows authors to specify online fonts to display text on their web pages. By allowing authors to provide their own fonts, @font-face eliminates the need to depend on the limited number of fonts users have installed on their computers.'
tags:
  - CSS
  - At
  - Rules
uri: css/atrules/@font-face

---
## Summary

The @font-face CSS at-rule allows authors to specify online fonts to display text on their web pages. By allowing authors to provide their own fonts, @font-face eliminates the need to depend on the limited number of fonts users have installed on their computers.

 The `@font-face` at-rule may be used not only at the top level of a CSS, but also inside any CSS conditional-group at-rule.

## Syntax

``` css
@font-face {
  [font-family: <family-name>;]?
  [src: [ <uri> [format(<string>#)]? | <font-face-name> ]#;]?
  [unicode-range: <urange>#;]?
  [font-variant: <font-variant>;]?
  [font-feature-settings: normal|<feature-tag-value>#;]?
  [font-stretch: <font-stretch>;]?
  [font-weight: <weight>];
  [font-style: <style>];
}
```

### Values

**\<family-name\>**
:   *Specifies a [**font-family**](/css/properties/font-family) name that will be used as font face value for font properties.*
**\<uri\>**
:   *The location of a font file to use (either an external reference with an optional hint or a local reference). To specify an external reference, use **url(sURL)**, where **sURL** is an absolute or relative URL. To specify specific font formats (only for externally referenced font files), use a **format** hint (**format(fontFormat)**) where **fontFormat** is a comma-separated list of format strings that denote supported font formats. Possible **fontFormat** values are **woff**, **truetype**, **opentype**, and **embedded-opentype**. The **format** hint is optional.*

<dl>
<dd>
*To specify a local reference, use **local(sFontName)**, where **sFontName** is the name of the locally-installed font to use. If that font is not found, other sources will be tried until one is found.*

</dd>
<dt>
**\<urange\>**

</dt>
<dd>
*A list of Unicode character ranges, where*urange*is a comma-separated list of Unicode range values.*

</dd>
<dt>
**\<font-variant\>**

</dt>
<dd>
*A [**font-variant**](/css/properties/font-variant) value.*

</dd>
<dt>
**\<font-stretch\>**

</dt>
<dd>
*A valid [**font-stretch**](/css/properties/font-stretch) property value.*

</dd>
<dt>
**\<weight\>**

</dt>
<dd>
*A valid [**font-weight**](/css/properties/font-weight) property value (except for the relative values, `bolder` and `lighter`).*

</dd>
<dt>
**\<style\>**

</dt>
<dd>
*A valid [**font-style**](/css/properties/font-style) property value.*

</dd>
</dl>
## Examples

The following example uses the Open Sans font to style the paragraph element.

``` css
/* Declare the font using @font-face. */
@font-face {
  font-family: "Open Sans";
  src: local("Open Sans"), /* Prefer a locally installed version of the font. */
       local("OpenSans"),
       /* URL requires a valid path to the respective font file.
          Same origin policy is applicable here.
       */
       url("/path/to/OpenSans.eot?#iefix") format("embedded-opentype"),
       url("/path/to/OpenSans.woff") format("woff"),
       url("/path/to/OpenSans.ttf") format("truetype"),
       url("/path/to/OpenSans.svg#OpenSans") format("svg");
  src: url("/path/to/OpenSans.eot");

  font-weight: normal;
  font-style: normal;
}

/* Use the font in your CSS as follows. */
p {
  font-family: "Open Sans", sans-serif;
}
```

[View live example](http://code.webplatform.org/gist/5481068)

## Usage

     Use this at-rule in order to use specific fonts that might not be available on your local system.

## Notes

The rule has no default value. The `unicode-range` descriptor defines the range of Unicode characters that are supported by a given font. The values of *urange* are expressed by hexadecimal numbers prefixed by "`U+`", that correspond\> to Unicode character code points. The `unicode-range` descriptor serves as a hint for the browser when it decides whether to download a font resource. Unicode range values are written by using hexadecimal values and are case insensitive. Each is prefixed by "`U+`" and multiple, discontinuous ranges are separated by commas. Whitespace before or after commas is ignored. Valid character code values vary between `0` and `10FFFF` inclusive. A single range has three basic forms:

-   A single code point (for instance, `U+416`)
-   An interval value range (for instance, `U+400-4ff`)
-   A range where trailing ‘`?`’ characters imply ‘any digit value’ (for instance, `U+4??`)

## Related specifications

[CSS Fonts Module Level 3](http://www.w3.org/TR/css3-fonts/)
:   Working Draft

## See also

### Related articles

#### Fonts

-   **@font-face**

-   [Font related properties](/css/fonts)

-   [font-variant](/css/fonts/font-variant)

-   [font](/css/properties/font)

-   [font-family](/css/properties/font-family)

-   [font-feature-settings](/css/properties/font-feature-settings)

-   [font-kerning](/css/properties/font-kerning)

-   [font-language-override](/css/properties/font-language-override)

-   [font-size](/css/properties/font-size)

-   [font-size-adjust](/css/properties/font-size-adjust)

-   [font-stretch](/css/properties/font-stretch)

-   [font-style](/css/properties/font-style)

-   [font-variant](/css/properties/font-variant)

-   [user-modify](/css/properties/user-modify)

-   [size](/html/attributes/size)

-   [font](/html/elements/font)

#### Syntax

-   [@charset](/css/atrules/@charset)

-   **@font-face**

-   [@import](/css/atrules/@import)

-   [@keyframes](/css/atrules/@keyframes)

-   [@namespace](/css/atrules/@namespace)

-   [@page](/css/atrules/@page)

-   [@supports](/css/atrules/@supports)

-   [CSS reference](/css/reference)

-   [Alphabetical list of CSS reference](/css/reference/alphabetical)

-   [!important](/css/syntax/!important)
