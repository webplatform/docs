---
title: accessKey
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/accessKeyEX.htm'
notes:
  - 'Needs updating, security considerations & clean up'
readiness: 'Out of Date'
summary: 'Sets a keyboard keystroke for selection of its element, which would otherwise be done using a mouse.'
tags:
  - Markup
  - Attributes
  - HTML
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/events/click
uri: html/attributes/accessKey

---
## Summary

Sets a keyboard keystroke for selection of its element, which would otherwise be done using a mouse.

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
## Examples

This example uses the **label** object and the **accessKey** attribute to set focus on a text box. The **label** object makes it possible to underline the designated **accessKey**. You may also use the [**-ms-accelerator**](/css/media_queries/accelerator) attribute to hide the underline until the ALT key is pressed.

``` html
<label for="fp1" accesskey="1">#<span style="text-decoration: underline;">1</span>:
Press ALT+1 to set focus to textbox</label>
<input type="text" name="T1" value="text1" size="20" tabindex="1" id="fp1">
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/accessKeyEX.htm)

## Notes

### Remarks

By default, pressing an access key sets focus to an object. The object receives focus when the user simultaneously presses the ALT key and the access key assigned to an object. Some controls perform an action after receiving focus. For example, using **accessKey** on an **input type=button** causes the [**onclick**](/w/index.php?title=dom/events/click&action=edit&redlink=1) event to fire. By comparison, applying the **accessKey** on a radio button causes the **onclick** event to fire and toggles the [**checked**](/html/attributes/checked) property, visibly selecting or deselecting the control. **Note**  For elements that are not tab stops by default, such as a **SPAN**, the [**tabIndex**](/html/attributes/tabIndex) property must be set on the element for the **accessKey** property to function. In Windows Internet Explorer 7 and greater, ALT+D selects text in the Address bar, making D unavailable as a keyboard shortcut on a webpage. As of Microsoft Internet Explorer 5, some scoped elements do not implicitly support the **accessKey** property. Instead, they support the property by setting the [**TABINDEX**](/html/attributes/tabIndex) attribute to any valid negative or positive integer.

### Syntax

## See also

### Related pages

-   `a`
-   `abbr`
-   `acronym`
-   `address`
-   `applet`
-   `area`
-   `article`
-   `aside`
-   `b`
-   `bdo`
-   `big`
-   `blockQuote`
-   `body`
-   `button`
-   `caption`
-   `center`
-   `cite`
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
-   `figcaption`
-   `figure`
-   `font`
-   `footer`
-   `header`
-   `hgroup`
-   `hn`
-   `hr`
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
-   `isIndex`
-   `kbd`
-   `label`
-   `legend`
-   `li`
-   `listing`
-   `mark`
-   `marquee`
-   `menu`
-   `nav`
-   `object`
-   `ol`
-   `p`
-   `plainText`
-   `pre`
-   `q`
-   `rt`
-   `ruby`
-   `s`
-   `samp`
-   `section`
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
-   `accelerator`
-   `tabIndex`
