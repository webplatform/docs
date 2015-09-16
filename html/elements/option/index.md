---
title: option
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Add Category, Parent and Children information. Complete Compatibility table. Complete HTML information subsection.'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLOptionElement](/dom/HTMLOptionElement)'
readiness: 'In Progress'
standardization_status: 'W3C Recommendation'
summary: 'Denotes one choice in a select element.'
tags:
  - Markup
  - Elements
  - HTML
uri: html/elements/option

---
## Summary

Denotes one choice in a select element.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLOptionElement](/dom/HTMLOptionElement)

## Attributes

-   `disabled` = boolean
    if present, disable a option.
-   `label` = string
    Provides a label for element.
    If there isn't, the label of an option element is the textContent of the element.
-   `value` = string
    Provides a value for element.
    If there isn't, the value of an option element is the textContent of the element.
-   `selected` = boolean
    Represents the default selectedness of the element. [[Example A]](#Example_A)

## Examples

This example uses the **OPTION** element to create individual items in a drop-down list box.

``` html
<!DOCTYPE html>
<html>
 <head>
  <title>Example</title>
 </head>
 <body>
  <select id="car-list" size="1">
   <option value="1">BMW</option>
   <option value="2">PORSCHE</option>
   <option value="3" selected>MERCEDES</option>
  </select>
  <textarea id="text-area"></textarea>
 </body>
</html>
```

Using the markup of the previous example, this JavaScript example uses the [**options**](/dom/HTMLElement/options) collection to append the selected item of the list box in a text area.

``` js
function appendCar() {
  var carListElement = document.getElementById("car-list");
   document.getElementById("text-area").value +=carListElement.options[carListElement.selectedIndex].text + "\n";
}
document.addEventListener("DOMContentLoaded", appendCar, false);
```

As a child of an optgroup element

``` html
<form action="courseselector.dll" method="get">
  <p>Which course would you like to watch today?
  <p><label>Course:
    <select name="c">
      <optgroup label="8.01 Physics I: Classical Mechanics">
        <option value="8.01.1">Lecture 01: Powers of Ten</option>
        <option value="8.01.2">Lecture 02: 1D Kinematics</option>
        <option value="8.01.3">Lecture 03: Vectors</option>
      </optgroup>
      <optgroup label="8.02 Electricity and Magnestism">
        <option value="8.02.1">Lecture 01: What holds our world together?</option>
        <option value="8.02.2">Lecture 02: Electric Field</option>
        <option value="8.02.3">Lecture 03: Electric Flux</option>
      </optgroup>
      <optgroup label="8.03 Physics III: Vibrations and Waves">
        <option value="8.03.1">Lecture 01: Periodic Phenomenon</option>
        <option value="8.03.2">Lecture 02: Beats</option>
        <option value="8.03.3">Lecture 03: Forced Oscillations with Damping</option>
      </optgroup>
    </select>
  </label>
  <p><input type=submit value="▶ Play">
</form></optgroup>
```

## Notes

You can create new **OPTION** elements dynamically with the [**document.createElement**](/dom/Document/createElement) method, but you cannot change properties until the new element is added to a **SELECT** object. Or, you can create fully formed elements by using the [**Option**](/dom/Option) object, as follows:

     var opt = new Option( 'Text', 'Value', fDefaultSelected );

You can add **OPTION** elements only to a **SELECT** element that is located in the same window where the **OPTION** elements are created. Except for [**background-color**](/css/properties/background-color) and [**color**](/css/properties/color), style settings applied through the [**style**](/css/cssom/style) object for the **option** element are ignored. In addition, style settings applied directly to individual [**options**](/dom/HTMLElement/options) override those applied to the containing **SELECT** element as a whole.

## Related specifications

[HTML 5.1](http://www.w3.org/TR/html51/forms.html#the-option-element)
:   W3C Working Draft

[HTML 5](http://www.w3.org/TR/html5/forms.html#the-option-element)
:   W3C Recommendation

[HTML 4.01](http://www.w3.org/TR/html401/interact/forms.html#edef-OPTION)
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

-   [input](/html/elements/input)

-   [ins](/html/elements/ins)

-   [kbd](/html/elements/kbd)

-   [legend](/html/elements/legend)

-   [mark](/html/elements/mark)

-   **option**

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
