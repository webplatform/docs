---
title: 'select'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: select
  topic: html
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLSelectElement](/dom/HTMLSelectElement)'
readiness: 'In Progress'
standardization_status: 'W3C Recommendation'
summary: 'The select element is used to create a drop-down list. Used with option tags inside the select element to define the available options in the list.'
tags:
  - Markup
  - Elements
  - HTML
uri: html/elements/select

---
## Summary

The select element is used to create a drop-down list. Used with option tags inside the select element to define the available options in the list.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLSelectElement](/dom/HTMLSelectElement)

## Attributes

-   `autofocus` = boolean
    Allows the author to indicate that a control is to be focused as soon as the page is loaded
-   `disabled` = boolean
    If present, make the control non-interactive and to prevent its value from being submitted.
-   `form` = the ID of a form element in the element's owner
    Associate the select element with its form owner.
    By default, the select element is associated with its nearest ancestor form element.
-   `multiple` = boolean
    If the attribute is present, then the select element represents a control for selecting zero or more options from the list of options. [[Example B]](#Example_B)
-   `name` = unique name
    Represents the element's name.
-   `required` = boolean
    When specified, the user will be required to select a value before submitting the form.
-   `size` = valid non-negative intege
    Gives the number of options to show to the user.
    If the multiple attribute is present, then the size attribute's default value is 4. If the multiple attribute is absent, then the size attribute's default value is 1.

## Internationalization

Internationalization topics related to the `select` element:

-   [Linking to localized content](http://www.w3.org/International/techniques/authoring-html#linkloc)
-   [Working with form controls](http://www.w3.org/International/techniques/authoring-html#formcontrols) (specifically sorting of select options)

## Examples

This example uses the **SELECT** element to create a drop-down list box.

``` html
<select name="Cats" size="1">
  <option value="1">Calico</option>
  <option value="2">Tortie</option>
  <option value="3" selected="">Siamese</option>
</select>
```

This example uses the **select** element to create a multi-select list box by setting the [**SIZE**](/html/attributes/size_(control)) and [**MULTIPLE**](/html/attributes/multiple) attributes. To retrieve the selected options for a multi-select list box, iterate through the [**options**](/dom/HTMLElement/options) collection and check to see where [**SELECTED**](/html/attributes/selected) is set to **true**.

``` html
<select id="select-element" name="cars" size="3" multiple="">
  <option value="1" selected="">BMW</option>
  <option value="2">Porsche</option>
  <option value="3" selected="">Mercedes</option>
</select>
```

This JavaScript example adds a new option to the end of the **SELECT** list created above. The [Option](/dom/Option) constructor can also be used in JavaScript.

``` js
var option = document.createElement("OPTION");
option.text="Ferrari";
option.value="4";
document.getElementById("select-element").add(option);
```

## Notes

In the Browser app for Android 4.1 (and possibly later versions), there is a bug where the menu indicator triangle on the side of a **select** will not be displayed if a `background`, `border`, or `border-radius` style is applied to the **select**.

Firefox for Android, by default, sets a `background-image` gradient on all `<select multiple>` elements. This can be disabled using `background-image: none`.

## Related specifications

[HTML 5.1](http://www.w3.org/TR/html51/forms.html#the-select-element)
:   W3C Working Draft

[HTML 5](http://www.w3.org/TR/html5/forms.html#the-select-element)
:   W3C Recommendation

[HTML 4.01](http://www.w3.org/TR/html401/interact/forms.html#edef-SELECT)
:   W3C Recommendation
