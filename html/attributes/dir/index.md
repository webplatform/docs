---
title: dir
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://www.w3.org/International/php/examples/generate?data=bidi&test=18'
notes:
  - 'Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info'
readiness: 'Not Ready'
standardization_status: 'W3C Recommendation'
summary: 'Global attribute. Specifies the element’s text directionality.'
tags:
  - Markup
  - Attributes
  - HTML
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - 'dom/properties/dir (Document object)'
uri: html/attributes/dir

---
## Summary

Global attribute. Specifies the element’s text directionality.

<table class="wikitable">
<tr>
<th>
Applies to

</th>
<td>
 ?

</td>
</tr>
</table>
dir = "ltr" or "rtl" or "auto"

Internationalization topics related to the `dir` attribute:

-   [Setting up a right-to-left page](http://www.w3.org/International/techniques/authoring-html#using)
-   [Setting direction on block elements](http://www.w3.org/International/techniques/authoring-html#blocks)
-   [Managing text direction in form controls](http://www.w3.org/International/techniques/authoring-html#formdir)
-   [Mixing text direction inline](http://www.w3.org/International/techniques/authoring-html#inline)
-   [Overriding the Unicode bidirectional algorithm](http://www.w3.org/International/techniques/authoring-html#bdo)

## Examples

For pages in Arabic, Hebrew, Persian, Thaana, Urdu, etc. set the default direction of the page to right-to-left by including dir in the html tag.

``` html
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
...
```

To make the exclamation mark appear to the left of the citation, surround the citation with markup and add a dir attribute.

``` html
<p>The title is "<span dir="rtl" lang="ar" xml:lang="ar">مفتاح معايير الويب!</span>" in Arabic.</p>
```

[View live example](http://www.w3.org/International/php/examples/generate?data=bidi&test=18)

## Notes

### Remarks

Unless explicitly set, the **dir** property has no return value when accessed in script. The property does not affect alphanumeric characters in Latin documents. These characters always render **ltr**. However, the property does affect punctuation characters in Latin documents. For example, punctuation marks such as periods and question marks render to the left of a sentence when the [**dir**](/w/index.php?title=dom/properties/dir_(Document_object)&action=edit&redlink=1) property is set to **rtl**. The real benefit of this attribute is when using **rtl** languages such as Arabic and Hebrew. These can be some of the most challenging languages to write **HTML** with especially because html in itself is a left-to-right programming language.

For more information see the following links:

-   [Text direction](http://www.w3.org/International/techniques/authoring-html#direction)
-   [Setting up a right-to-left page](http://www.w3.org/International/techniques/authoring-html#using)
-   [Setting direction on block elements](http://www.w3.org/International/techniques/authoring-html#blocks)
-   [Mixing text direction inline](http://www.w3.org/International/techniques/authoring-html#inline)
-   [Handling parentheses and other mirrored characters](http://www.w3.org/International/techniques/authoring-html#mirrored)

### Syntax

## See also

### Related pages (MSDN)

-   `a`
-   `abbr`
-   `acronym`
-   `address`
-   `area`
-   `b`
-   `bdo`
-   `big`
-   `blockQuote`
-   `body`
-   `button`
-   `caption`
-   `center`
-   `cite`
-   `code`
-   `col`
-   `colGroup`
-   `custom`
-   `dd`
-   `del`
-   `dfn`
-   `dir`
-   `div`
-   `dl`
-   `dt`
-   `em`
-   `embed`
-   `fieldSet`
-   `font`
-   `form`
-   `hn`
-   `html`
-   `i`
-   `img`
-   `input type=button`
-   `input type=checkbox`
-   `input type=file`
-   `input type=image`
-   `input type=password`
-   `input type=radio`
-   `input type=reset`
-   `input type=submit`
-   `input type=text`
-   `ins`
-   `kbd`
-   `label`
-   `legend`
-   `li`
-   `listing`
-   `map`
-   `marquee`
-   `menu`
-   `noBR`
-   `object`
-   `ol`
-   `optGroup`
-   `option`
-   `p`
-   `plainText`
-   `pre`
-   `q`
-   `rt`
-   `ruby`
-   `s`
-   `samp`
-   `select`
-   `small`
-   `span`
-   `strike`
-   `strong`
-   `sub`
-   `sup`
-   `table`
-   `tBody`
-   `td`
-   `textArea`
-   `tFoot`
-   `th`
-   `tHead`
-   `tr`
-   `tt`
-   `u`
-   `ul`
-   `var`
-   `xmp`
-   `Reference`
-   `direction`
-   `Conceptual`
-   `HTML Character Sets`
