---
title: style
code_samples:
  - 'http://result.dabblet.com/gist/11015343/6a6bb418f06ead5f7d21245426820c7df47dc228'
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Sets an inline style for the element.'
tags:
  - Markup
  - Attributes
  - HTML
uri: html/attributes/style

---
## Summary

Sets an inline style for the element.

<table class="wikitable">
<tr>
<th>
Applies to

</th>
<td>
dom/HTMLElement

</td>
</tr>
</table>
This attribute is used to set styling in the form of [CSS rules](http://docs.webplatform.org/wiki/guides/getting_started_with_css#Defining_style_rules) to an element.

## Examples

``` html
<!doctype html>
<title>HTML Style Attribute Usage</title>
<p style="background-color: blue; color: white;">This will be white text with a blue background.</p>
```

[View live example](http://result.dabblet.com/gist/11015343/6a6bb418f06ead5f7d21245426820c7df47dc228)

## Usage

     While this is perfectly valid, it is *highly* recommended by the community at large that you not use inline styles. Instead it is much better to simply target the element you want in your CSS and apply rules in there.

## Notes

### Remarks

This attribute is not accessible through scripting. To access styles through scripting, use the [**style**](/css/cssom/style) object.

## Related specifications

[HTML4 Specification](http://www.w3.org/TR/html401/present/styles.html)
:   W3C Recommendation
