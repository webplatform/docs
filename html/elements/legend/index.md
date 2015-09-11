---
title: legend
code_samples:
  - 'http://gist.github.com/8e4305d9f7fb613410a5'
notes:
  - 'Add Compatibility.'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLLegendElement](/dom/HTMLLegendElement)'
readiness: 'In Progress'
summary: 'The legend element represents a title or explanatory caption for the contents of its parent fieldset element.'
tags:
  - Markup
  - Elements
  - HTML
uri: html/elements/legend

---
## <span>Summary</span>

The legend element represents a title or explanatory caption for the contents of its parent fieldset element.

## <span>Overview Table</span>

[DOM Interface](/dom/interface)
:   [HTMLLegendElement](/dom/HTMLLegendElement)

The **legend** element represents a caption for the the contents of the legend element's parent fieldset element, if any.

## <span>Examples</span>

Simple form with fieldset, legend, and label elements.

``` html
<form action="" method="post">
  <fieldset>
    <legend>User credentials</legend>
    <label for="username">Username</label>
    <input type="text" name="username" id="username">
    <label for="password">Password</label>
    <input type="password" name="password" id="password">
  </fieldset>
</form>
```

[View live example](http://code.webplatform.org/gist/8e4305d9f7fb613410a5)

## <span>Usage</span>

     Generally, the legend element can be used in combination with a fieldset element when a group of form elements needs a caption. Pretty similar to a headline element but the legend element is the most semantic element in that case.

## <span>Notes</span>

The first **legend** element in a **fieldset** is used as the caption of the **fieldset**. Additional **legend** elements are ignored.

The **legend** element will be placed within the border of the **fieldset** element if you are using a fieldset and leaving the default browser styles untouched. The position will change as soon as you set `border: none;` to your fieldset.

The »problem« with the **fieldset** and **legend** elements is that they don’t behave like normal block/inline elements. A general workaround with any styling and position issues (especially in old IEs) is to wrap your legends content with another element.

``` html
<fieldset>
  <legend><span>Legend link</span></legend>
</fieldset>
```

## <span>Related specifications</span>

[HTML 5.1](http://www.w3.org/TR/html51/forms.html#the-legend-element)
:   W3C Working Draft

[HTML 5](http://www.w3.org/TR/html5/forms.html#the-legend-element)
:   W3C Recommendation

[HTML 4.01](http://www.w3.org/TR/html401/interact/forms.html#edef-LEGEND)
:   W3C Recommendation

## <span>See also</span>

### <span>Related articles</span>

#### <span>HTML</span>

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

-   **legend**

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

### <span>Other articles</span>

-   [**form**](/html/elements/form) element
-   [**fieldset**](/html/elements/fieldset) element

### <span>External resources</span>

-   <http://www.w3.org/TR/html-markup/legend.html#legend>
-   <http://www.w3.org/TR/html5/forms.html#the-legend-element>
-   <http://www.w3.org/TR/html5/rendering.html#the-fieldset-and-legend-elements>
-   <http://morten.dk/blog/fieldset-legend-behave>
