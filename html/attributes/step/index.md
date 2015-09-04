---
title: step
tags:
  - Markup
  - Attributes
  - HTML
readiness: 'Not Ready'
standardization_status: 'W3C Recommendation'
notes:
  - 'Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info'
summary: 'Specify the increment for input with types number, time, or range'
code_samples:
  - 'http://jsfiddle.net/mejarc/YkGZY/2/'
  - 'http://jsfiddle.net/mejarc/YkGZY/6/'
uri: html/attributes/step

---
# step

## Summary

Specify the increment for input with types number, time, or range

Applies to
:   [HTMLInputElement](/html/elements/input)

When `input type="range"`, `input type="date"`, or `input type="number"` is specified, the default increment from `min` to `max` is 1. Override this default with a value in `step`.

## Examples

A slider with a range from 1-12 that increments by 3.

``` {.html}
<input type="range" min="1" max="24" step="3" />
```

A form input for a number between 0 and 15 that increments by 3.

``` {.html}
<input type="number" min="0" max="15" step="3" />​​​​​​​​​​​​​​​​​​​​
```

[View live example](http://jsfiddle.net/mejarc/YkGZY/2/)

Restricting time input to half-hours.

``` {.html}
<input type="time"  step="1800" />
```

[View live example](http://jsfiddle.net/mejarc/YkGZY/6/)

## Usage

     * when used for input type="time", value must be in seconds

## Notes

### Remarks

The following example shows the use of the [**min**](/html/attributes/min), [**max**](/html/attributes/max_(HTMLInputElement)), and **step** attributes.

### Syntax

### Standards information

-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374), Section 4.10.7.3.11

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

-   **step**

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

### External resources

-   [http://dev.opera.com/articles/view/new-form-features-in-html5/\#input-datetime](http://dev.opera.com/articles/view/new-form-features-in-html5/#input-datetime)
-   [http://www.quirksmode.org/html5/inputs.html](http://www.quirksmode.org/html5/inputs.html)

### Related pages (MSDN)

-   `HTMLInputElement`
-   `input type=number`
-   `input type=range`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/HTML/Element/Input#Attributes)

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

This content was originally published on [DevOpera](http://dev.opera.com), Opera's Developer Network. .

