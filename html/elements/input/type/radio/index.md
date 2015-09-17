---
title: 'radio'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: radio
  topic: html
notes:
  - 'Merge Candidate: html/attributes/type'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLInputElement](/dom/HTMLInputElement)'
readiness: 'Not Ready'
summary: 'The radio type of the &lt;input&gt; element represents a radio button control.'
tags:
  - Pages_using_duplicate_arguments_in_template_calls
  - Markup_Elements
  - HTML
uri: html/elements/input/type/radio

---
## Summary

The radio type of the &lt;input&gt; element represents a radio button control.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLInputElement](/dom/HTMLInputElement)

## Examples

This example uses the \<label\> tag to include the text with the checkbox to increase the touch sensitive area of the checkbox.

``` html
<label><input id="red" type="checkbox" name="colors" value="red" />Text</label>
```

This example uses the **INPUT type=radio** element to create three radio buttons.

``` html
<INPUT type=radio name="radio" CHECKED>1-10 years old
<INPUT type=radio name="radio">11 years old
<INPUT type=radio name="radio">12-120 years old
```

This example uses script to detect which radio button the user selects.

``` html
<SCRIPT>
function detect()
{
    if (radio[0].checked)
        alert("You're between 1 and 10 years old.")
    else if (radio[1].checked)
        alert("You're 11 years old.")
    else
        alert("You're between 12 and 120 years old.")
}
</SCRIPT>
```

## Notes

### Remarks

Use a radio button control to limit a user's selection to a single value within a set of values. To do this, you must link together each button in a set of radio buttons by assigning each button the same [**name**](/html/attributes/name). When a user submits a form, a selected radio button generates a name/value pair in the form data only if the button has a [**value**](/html/attributes/value_(select,_option_element)). To select a radio button as the default button in a set, set the [**checked**](/html/attributes/checked) property of the button to `true`. A user can select a radio button only if the button has a [**name**](/html/attributes/name). To clear a selected radio button, a user must select another button in the set. Windows Internet Explorer 8 and later. In IE8 Standards mode, you can select an **input type=radio** button that does not have a [**name**](/html/attributes/name) attribute specified. In addition, dynamically setting the **name** attribute on an **input type=radio** button correctly applies that button to the same named group. For more information, see Defining Document Compatibility. Touching on the label associated with a radio button has the same effect as touching the radio button directly.

### Standards information

-   [HTML 4.01 Specification](http://go.microsoft.com/fwlink/p/?linkid=25320), Section 17.4

### HTML information

{

## See also

### Related pages

-   `Reference`
-   `input`
-   `Conceptual`
-   `Introduction to Forms`
