---
title: fieldset
tags:
  - Markup
  - Elements
  - HTML
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'The fieldset element is used to group related fields within a form.'
code_samples:
  - 'http://gist.github.com/f77f0a06304503ecddd6'
  - 'http://gist.github.com/fc26d3507ee33bdd6043'
  - 'http://gist.github.com/91bca1371d394bf3c52d'
uri: html/elements/fieldset

---
# fieldset

## Summary

The fieldset element is used to group related fields within a form.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLFieldSetElement](/dom/HTMLFieldSetElement)

The *fieldset* element represents a set of form controls. Optionally given a name with a child **legend** element.

### attributes

**NOTE**: Those attributes are considered valid since HTML5

 disabled�
:   If this Boolean attribute is set, the form controls that are its descendants, except descendants of its first optional **legend** element, are disabled, i.e., not editable. They won't receive any browsing events, like mouse clicks or focus-related ones. Often browsers display such controls as gray.
 form�
:   This attribute has the value of the id attribute of the **form** element its related to. Its default value is the id of the nearest \<form\> element it is a descendant of.
 name�
:   The name associated with the group. This is for use in the `form.elements` API.

## Examples

Simple form with fieldset, legend, and label elements.

``` {.html}
<form action="" method="post">
  <fieldset>
    <legend>Title</legend>
    <label for="radio">Click me</label>
    <input type="radio" name="radio" id="radio">
  </fieldset>
</form>
```

[View live example](http://code.webplatform.org/gist/f77f0a06304503ecddd6)

The following snippet shows a **fieldset** with a checkbox in the legend that controls whether or not the fieldset is enabled.

``` {.html}
<form>
  <fieldset name="clubfields" disabled>
    <legend>
      <label for="club">Use Club Card</label>
      <input type="checkbox" id="club" name="club" onchange="form.clubfields.disabled = !checked">
    </legend>

     <label for="clubname">Name on card:</label>
     <input name="clubname" type="text">
```

         <label for="clubnum">Card number:</label>
         <input name="clubnum" type="number">

         <label for="clubnum">Expiry date:</label>
         <input name="clubexp" type="date">

     </fieldset>

\</form\>

</pre>
[View live example](http://code.webplatform.org/gist/fc26d3507ee33bdd6043)

</div>
Example with nested **fieldset** elements.

``` {.html}
<form action="">
  <fieldset name="clubfields" disabled>
    <legend>
      <label for="club">Use Club Card</label>
      <input type="checkbox" name="club" id="club" onchange="form.clubfields.disabled = !checked">
    </legend>

     <label for="">Name on card:</label>
     <input name="clubname">
```

       <fieldset name="numfields">
         <legend>
           <label for="clubtype">My card has numbers on it</label>
           <input type="radio" checked name="clubtype" id="clubtype" onchange="form.numfields.disabled = !checked">
         </legend>

           <label for="clubnum">Card number:</label>
           <input name="clubnum" id="clubnum" type="text">

       </fieldset>
       <fieldset name="letfields" disabled>
         <legend>
           <label>My card has letters on it</label>
           <input type="radio" name="clubtype" id="clubtype" onchange="form.letfields.disabled = !checked">
         </legend>

           <label for="clublet">Card code:</label>
           <input name="clublet" id="clublet">

       </fieldset>
     </fieldset>

\</form\>

</pre>
[View live example](http://code.webplatform.org/gist/91bca1371d394bf3c52d)

</div>
## Usage

     Fieldsets are not required but useful for grouping elements in a form to enhance the visual flow and usability of complex forms. optionally you can use a legend element to give your fieldset element a caption.

## Notes

### Default layout

Typically, the browser draws a box around the containing elements of every fieldset. This border can be disabled via CSS `border: none;` The border contains the legend by default. See [**legend**](/html/elements/legend) for details.

The ["Rendering" section of the WHATWG HTML specification](https://html.spec.whatwg.org/multipage/rendering.html#the-fieldset-and-legend-elements) suggests [`min-width`](/css/properties/min-width)`: min-content` as part of the default style for **fieldset**, and many browsers implement such styling (or something that approximates it); almost no other element shares this default style. See also [StackOverflow](http://stackoverflow.com/questions/17408815/fieldset-resizes-wrong-appears-to-have-unremovable-min-width-min-content), [Mozilla bug \#504622](https://bugzilla.mozilla.org/show_bug.cgi?id=504622), and [WebKit bug \#123507](https://bugs.webkit.org/show_bug.cgi?id=123507).

### Nesting fieldsets

It’s also possible and in certain use cases pretty useful to nest fieldsets.

### Compatibility

Not all form control descendants of a disabled **fieldset** are properly disabled in IE11; see [IE bug 817488: `input[type="file"]` not disabled inside disabled `fieldset`](https://connect.microsoft.com/IE/feedbackdetail/view/817488) and [IE bug 962368: Can still edit `input[type="text"]` within `fieldset[disabled]`](https://connect.microsoft.com/IE/feedbackdetail/view/962368/can-still-edit-input-type-text-within-fieldset-disabled).

## Related specifications

Specification
:   Status
[HTML 5.1](http://www.w3.org/TR/html51/forms.html#the-fieldset-element)
:   W3C Working Draft
[HTML 5](http://www.w3.org/TR/html5/forms.html#the-fieldset-element)
:   W3C Recommendation
[HTML 4.01](http://www.w3.org/TR/html401/interact/forms.html#edef-FIELDSET)
:   W3C Recommendation

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

-   **fieldset**

-   [font](/html/elements/font)

-   [footer](/html/elements/footer)

-   [head](/html/elements/head)

-   [hn](/html/elements/hn)

-   [hr](/html/elements/hr)

<!-- -->

    … further results

### Other articles

-   [**legend**](/html/elements/legend) element
-   [**form**](/html/elements/form) element

### External resources

-   [http://www.w3.org/TR/html5/forms.html\#the-fieldset-element](http://www.w3.org/TR/html5/forms.html#the-fieldset-element)
-   [http://www.w3.org/TR/html5/rendering.html\#the-fieldset-and-legend-elements](http://www.w3.org/TR/html5/rendering.html#the-fieldset-and-legend-elements)
-   [http://www.w3.org/TR/html-markup/fieldset.html\#fieldset](http://www.w3.org/TR/html-markup/fieldset.html#fieldset)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/fieldset)

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

