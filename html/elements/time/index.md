---
title: time
notes:
  - 'Add compatibility, list valid values'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLTimeElement](/w/index.php?title=dom/HTMLTimeElement&action=edit&redlink=1)'
readiness: 'Almost Ready'
standardization_status: 'W3C Recommendation'
summary: "The time tag defines either a time (24 hour clock), or a date in the Gregorian calendar, optionally with a time and a time-zone offset. It does not render differently in any of the major browsers.\n"
tags:
  - Markup
  - Elements
  - HTML
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/HTMLTimeElement
uri: html/elements/time

---
## Summary

The time tag defines either a time (24 hour clock), or a date in the Gregorian calendar, optionally with a time and a time-zone offset. It does not render differently in any of the major browsers.

This element can be used as a way to encode dates and times in a machine-readable way so that, for example, user agents can offer to add birthday reminders or scheduled events to the user's calendar.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLTimeElement](/w/index.php?title=dom/HTMLTimeElement&action=edit&redlink=1)

The HTML time element (<time>) represents either time on a 24-hour clock or a precise date in the Gregorian calendar (with optional time and timezone information). </time>

This element is intended to be used presenting dates and times in a machine readable format. This can be helpful for user agents to offer any event scheduling for user's calendar.

## Attributes

-   `datetime` = date or time
    Specifies the date or time that the element represents.

## Validity

The datetime value of a time element is the value of the element's datetime attribute, if it has one, or the element's textContent, if it does not.

The kind of content is limited to various kinds of dates, times, time-zone offsets, and durations, as described below:

-   A valid month string
    -   2012-03
-   A valid date string
    -   3012-03-29
-   A valid time string
    -   15:25
    -   15:25:35
-   A valid local date and time string
    -   2012-03-29T15:25:35
    -   2012-03-29 15:25:35
-   A valid time-zone offset string
    -   Z
    -   0000
    -   00:00
    -   See more details: [Datetime value](http://www.w3.org/TR/html5/the-time-element.html#datetime-value) at HTML5 specification.

## Examples

``` html
<p>
On <time datetime="1913-03-12">12 March 1913</time>, the city of Canberra
was officially given its name by Lady Denman, the wife of Governor-General
Lord Denman.
</p>
```

## Related specifications

[HTML 5.1](http://www.w3.org/TR/html51/text-level-semantics.html#the-time-element)
:   W3C Working Draft

[HTML 5](http://www.w3.org/TR/html5/text-level-semantics.html#the-time-element)
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

-   **time**

### External resources

-   [time page at the Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/HTML/HTML_Elements/time).

