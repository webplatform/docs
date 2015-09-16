---
title: 'value'
notes:
  - 'Just a final review is probably needed.'
readiness: 'Almost Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/HTMLTextAreaElement
    href: /dom/HTMLTextAreaElement
  return:
    predicate: 'Returns an object of type '
    value: String
    href: /dom/HTMLTextAreaElement
standardization_status: 'W3C Recommendation'
summary: 'Gets the content of a &lt;textarea&gt; element.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/HTMLTextAreaElement/value

---
## Summary

Gets the content of a &lt;textarea&gt; element.

Property of [dom/HTMLTextAreaElement](/dom/HTMLTextAreaElement)[dom/HTMLTextAreaElement](/dom/HTMLTextAreaElement)

## Syntax

``` js
var textAreaContent = textAreaElement.value;
textAreaElement.value = newTextAreaContent;
```

## Return Value

Returns an object of type StringString

The content of the element, whether entered, existing or otherwise visible.

## Examples

The following code uses this property to log the content of a `<textarea>` and its length.

``` js
// Declaring the used variables first.
var textAreaList, textArea;

// Getting any <textarea> in the page
textAreaList = document.getElementsByTagName("textarea");

// Verifying there is at least one.
if (textAreaList.length) {

    // Getting the first <textarea> in the page.
    textArea = textAreaList[0];

   // Logging the content of the first <textarea> in the page.
    console.log("The content of the first textarea element is - " +
        textArea.value);

    // Logging the codepoint length of the
    // content of the first <textarea> in the page.
    console.log("The codepoint length of the content of the first textarea element is - " +
        textArea.value.length);
}
```

## Usage

     Use this property to get the content of <textarea>.

## Notes

In JavaScript/ECMAScript, the [length](/javascript/String/length) property of this property can be used to determine the codepoint length of the content.

## Related specifications

[Document Object Model (DOM) Level 1](http://www.w3.org/TR/REC-DOM-Level-1/level-one-html.html#ID-70715579)
:   W3C Recommendation

[Document Object Model (DOM) Level 2 HTML](http://www.w3.org/TR/DOM-Level-2-HTML/html.html#ID-70715579)
:   W3C Recommendation

[W3C HTML5](http://www.w3.org/TR/html/forms.html#dom-textarea-value)
:   W3C Candidate Recommendation

[WHATWG HTML](http://www.whatwg.org/specs/web-apps/current-work/multipage/forms.html#dom-textarea-value)
:   Living Standard

## See also

### Related articles

#### HTML

-   [user-modify](/css/properties/user-modify)

-   [textLength](/dom/HTMLTextAreaElement/textLength)

-   **value**

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
