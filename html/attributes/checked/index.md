---
title: checked
tags:
  - Markup
  - Attributes
  - HTML
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Indicates the initial state of a checkbox or radio button.'
code_samples:
  - 'http://gist.github.com/7282321'
  - 'http://gist.github.com/33aa4c8bece121ba6e9e'
uri: html/attributes/checked
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/properties/defaultChecked
    - dom/methods/removeAttribute
    - dom/methods/setAttribute

---
# checked

## Summary

Indicates the initial state of a checkbox or radio button.

Applies to
:   [html/elements/input](/html/elements/input)

The checked attribute can be used to specify what the visual or initial state of an input element is. It's often used to toggle an element through JavaScript.

As a boolean attribute, valid values are "`checked`" and nothing. The attribute is never required.

## Examples

This example shows a set of radio buttons with one checked by default.

``` {.html}
<form>
    <fieldset>
        <legend>Radio buttons</legend>
        <input type="radio" name="rad" id="rad1" value="Option 1">
        <label for="rad1">Option 1</label>
        <input type="radio" name="rad" id="rad2" value="Option 2" checked>
        <label for="rad2">Option 2</label>
        <input type="radio" name="rad" id="rad3" value="Option 3">
        <label for="rad3">Option 3</label>
        <input type="radio" name="rad" id="rad4" value="Option 4">
        <label for="rad4">Option 4</label>
    </fieldset>
</form>
```

[View live example](http://code.webplatform.org/gist/7282321)

This example shows a set of check boxes with multiple checked by default.

``` {.html}
<form>
    <fieldset>
        <legend>Check boxes</legend>
        <input type="checkbox" name="check1" id="check1" value="Option 1">
        <label for="check1">Option 1</label>
        <input type="checkbox" name="check2" id="check2" value="Option 2" checked>
        <label for="check2">Option 2</label>
        <input type="checkbox" name="check3" id="check3" value="Option 3">
        <label for="check3">Option 3</label>
        <input type="checkbox" name="check4" id="check4" value="Option 4" checked>
        <label for="check4">Option 4</label>
    </fieldset>
</form>
```

[View live example](http://code.webplatform.org/gist/33aa4c8bece121ba6e9e)

## Notes

### Remarks

Check boxes that are not selected do not return their values when the **form** is submitted.

A user can select a radio button only if the button has a [**name**](/html/attributes/name). A set of radio buttons is defined by the same value for the **name** attribute. To clear a selected radio button, a user must select another button in the set. One radio button in a set should always be checked, else the form is invalid by default. Only the value of the selected radio button is returned when the **form** is submitted.

Windows Internet Explorer 8 and later. In IE8 Standards mode, parsing operations on the **checked** content attribute always affect both the **checked** content attribute and [**defaultChecked**](/w/index.php?title=dom/properties/defaultChecked&action=edit&redlink=1) Document Object Model (DOM) attribute. For example, [**removeAttribute('checked')**](/w/index.php?title=dom/methods/removeAttribute&action=edit&redlink=1) sets both **checked** and **defaultChecked** to false. Similarly, [**setAttribute('checked', 'checked')**](/w/index.php?title=dom/methods/setAttribute&action=edit&redlink=1) sets both DOM attributes to true (as if the element was being re-parsed) For more information on IE8 mode, see Defining Document Compatibility. Internet Explorer 8 and later. In IE8 mode, the [**defaultChecked**](/w/index.php?title=dom/properties/defaultChecked&action=edit&redlink=1) DOM attribute reflects the value of the **checked** content attribute.

## Related specifications

Specification
:   Status
[HTML5](http://www.w3.org/TR/html5/forms.html#attr-input-checked)
:   W3C Candidate Recommendation

## See also

### Related articles

#### HTML

-   [user-modify](/css/properties/user-modify)

-   [HTMLAudioElement](/dom/HTMLAudioElement)

-   [textLength](/dom/HTMLTextAreaElement/textLength)

-   [value](/dom/HTMLTextAreaElement/value)

-   [accept](/html/attributes/accept)

-   [action](/html/attributes/action)

-   [alt](/html/attributes/alt)

-   [autocomplete](/html/attributes/autocomplete)

-   [autofocus](/html/attributes/autofocus)

-   **checked**

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

<!-- -->

    … further results

### Other articles

-   [**checkbox**](/html/elements/input/type/checkbox) element
-   [**radio**](/html/elements/input/type/radio) element

### External resources

-   [http://www.w3.org/TR/html-markup/input.radio.html](http://www.w3.org/TR/html-markup/input.radio.html)
-   [http://www.w3.org/TR/html-markup/input.checkbox.html](http://www.w3.org/TR/html-markup/input.checkbox.html)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

