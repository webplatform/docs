---
title: input
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/6364130'
notes:
  - "Add Category, Parent, Children and Compatibility information.\nIs size=\"20,5\" valid?"
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLInputElement](/dom/HTMLInputElement)'
readiness: 'In Progress'
standardization_status: 'W3C Recommendation'
summary: 'The input element (&lt;input/&gt;) is a multipurpose element for representing form widgets. The type of widget depends on the type attribute.'
tags:
  - Markup
  - Elements
  - HTML
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - html/attributes/dirname
    - html/attributes/formaction
    - html/attributes/formenctype
    - html/attributes/formmethod
    - html/attributes/formnovalidate
    - html/attributes/value
uri: html/elements/input

---
## Summary

The input element (&lt;input/&gt;) is a multipurpose element for representing form widgets. The type of widget depends on the type attribute.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLInputElement](/dom/HTMLInputElement)

The input element behavior varies depending on the value of its [type](/html/elements/input/type) attribute:

-   [type=button](/html/elements/input/type/button)
-   [type=checkbox](/html/elements/input/type/checkbox)
-   [type=color](/html/elements/input/type/color)
-   [type=date](/html/elements/input/type/date)
-   [type=datetime-local](/html/elements/input/type/datetime-local)
-   [type=email](/html/elements/input/type/email)
-   [type=file](/html/elements/input/type/file)
-   [type=hidden](/html/elements/input/type/hidden)
-   [type=image](/html/elements/input/type/image)
-   [type=month](/html/elements/input/type/month)
-   [type=number](/html/elements/input/type/number)
-   [type=password](/html/elements/input/type/password)
-   [type=radio](/html/elements/input/type/radio)
-   [type=range](/html/elements/input/type/range)
-   [type=reset](/html/elements/input/type/reset)
-   [type=time](/html/elements/input/type/time)
-   [type=search](/html/elements/input/type/search)
-   [type=submit](/html/elements/input/type/submit)
-   [type=tel](/html/elements/input/type/tel)
-   **[type=text](/html/elements/input/type/text)** (default if type is not set or empty)
-   [type=url](/html/elements/input/type/url)
-   [type=week](/html/elements/input/type/week)

Other valid attributes for the input element are `accept`, `alt`, `autocomplete`, `autofocus`, `checked`, `dirname`, `disabled`, `form`, `formaction`, `formenctype`, `formmethod`, `formnovalidate`, `formtarget`, `height`, `list`, `max`, `maxlength`, `min`, `multiple`, `name`, `pattern`, `placeholder`, `readonly`, `required`, `size`, `src`, `step`, `value`, `width`, and global element attributes. Note that some attributes do not apply for certain types.

Internationalization topics related to the `input` element:

-   [Managing text direction in form controls](http://www.w3.org/International/techniques/authoring-html#formdir)
-   [Working with date formats](http://www.w3.org/International/techniques/authoring-html#localdata)
-   [Working with personal names](http://www.w3.org/International/techniques/authoring-html#localnames)

## Examples

This example uses the **input** element to create different types of input controls.

``` html
<form action="http://example.org/survey" method="post">
<p>Name</p>
<br/><input name="control1" type="text" value="Your Name"/>
<p>Password</p>
<br><input type="password" name="control2"/>
<p>Color</p>
<br><input type="radio" name="control3" value="0" checked="checked"/>Red
<input type="radio" name="control3" value="1"/>Green
<input type="radio" name="control3" value="2"/>Blue
<p>Comments</p>
<br/><input type="text" name="control4" size="20,5" maxlength="250"/>
<p><input name="control5" type=checkbox checked>Send receipt</p>
<p><input type="submit" value="OK"/><input type="reset" value="reset"/></p>
</form>
```

[View live example](http://code.webplatform.org/gist/6364130)

## Usage

     To cater for international users see: Managing text direction in form controls

## Notes

For code samples, see [Form controls part 1](http://go.microsoft.com/fwlink/p/?LinkID=251128) and [Form controls part 2: validation](http://go.microsoft.com/fwlink/p/?LinkID=251131) on the Windows Internet Explorer sample site.

Firefox will, unlike other browsers, by default, [persist the dynamic disabled state and (if applicable) dynamic checkedness](http://stackoverflow.com/questions/5985839/bug-with-firefox-disabled-attribute-of-input-not-resetting-when-refreshing) of an **input** across page loads. Setting the value of the `autocomplete` attribute to `off` disables this feature; this works even when the `autocomplete` attribute would normally not apply to the **input** by virtue of its `type`. See [Mozilla bug \#654072](https://bugzilla.mozilla.org/show_bug.cgi?id=654072).

Safari Mobile for iOS applies a default style of [`opacity`](/css/properties/opacity)`: 0.4` to disabled textual **input** elements. Other major browsers don't currently share this particular default style.

## Related specifications

[HTML 5.1](http://www.w3.org/TR/html51/forms.html#the-input-element)
:   W3C Working Draft

[HTML 5](http://www.w3.org/TR/html5/forms.html#the-input-element)
:   W3C Recommendation

[HTML 4.01](http://www.w3.org/TR/html401/interact/forms.html#edef-INPUT)
:   W3C Recommendation

## See also

### Related articles

#### HTML

-   [user-modify](/css/properties/user-modify)

-   [textLength](/dom/HTMLTextAreaElement/textLength)

-   [value](/dom/HTMLTextAreaElement/value)

-   [accept](/html/attributes/accept)

-   [action](/html/attributes/action)

-   [alt](/html/attributes/alt)

-   [autocomplete](/html/attributes/autocomplete)

-   [autofocus](/html/attributes/autofocus)

-   [checked](/html/attributes/checked)

-   [crossorigin](/html/attributes/crossorigin)

-   [form](/html/attributes/form)

-   [formEnctype](/html/attributes/formEnctype)

-   [height](/html/attributes/height)

-   [list](/html/attributes/list)

-   [max (HTMLInputElement)](/html/attributes/max_(HTMLInputElement))

-   [maxLength](/html/attributes/maxLength)

-   [min](/html/attributes/min)

-   [multiple](/html/attributes/multiple)

-   [readonly](/html/attributes/readonly)

-   [size](/html/attributes/size)

-   [standby](/html/attributes/standby)

-   [step](/html/attributes/step)

-   [HTML Elements](/html/elements)

-   [!DOCTYPE](/html/elements/!DOCTYPE)

-   [!DOCTYPE](/html/elements/!DOCTYPE/ja)

-   [acronym](/html/elements/acronym)

-   [b](/html/elements/b)

-   [b](/html/elements/b/ja)

-   [br](/html/elements/br)

-   [br](/html/elements/br/ja)

-   [button](/html/elements/button)

-   [button](/html/elements/button/ja)

-   [caption](/html/elements/caption)

-   [cite](/html/elements/cite)

-   [code](/html/elements/code)

-   [col](/html/elements/col)

-   [colgroup](/html/elements/colgroup)

-   [datalist](/html/elements/datalist)

-   [del](/html/elements/del)

-   [dfn](/html/elements/dfn)

-   [div](/html/elements/div)

-   [em](/html/elements/em)

-   [EMBED](/html/elements/embed)

-   [fieldset](/html/elements/fieldset)

-   [font](/html/elements/font)

-   [footer](/html/elements/footer)

-   [head](/html/elements/head)

-   [hn](/html/elements/hn)

-   [hr](/html/elements/hr)

-   [html](/html/elements/html)

-   [i](/html/elements/i)

-   [img](/html/elements/img)

-   **input**

-   [ins](/html/elements/ins)

-   [kbd](/html/elements/kbd)

-   [legend](/html/elements/legend)

-   [mark](/html/elements/mark)

-   [option](/html/elements/option)

-   [p](/html/elements/p)

-   [samp](/html/elements/samp)

-   [script](/html/elements/script)

-   [span](/html/elements/span)

-   [strong](/html/elements/strong)

-   [table](/html/elements/table)

-   [tbody](/html/elements/tbody)

-   [td](/html/elements/td)

-   [tfoot](/html/elements/tfoot)

-   [th](/html/elements/th)

-   [time](/html/elements/time)

### External resources

<http://www.w3.org/TR/html-markup/input.html#input>
