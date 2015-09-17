---
title: 'input'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs summary and compat'
readiness: 'In Progress'
standardization_status: 'W3C Recommendation'
tags:
  - Events
  - Needs_Summary
uri: dom/Element/input

---
## Overview Table

<table class="wikitable">
<tr>
<th>
Synchronous

</th>
<td>
No

</td>
</tr>
<tr>
<th>
Bubbles

</th>
<td>
No

</td>
</tr>
<tr>
<th>
Target

</th>
<td>
dom/Element

</td>
</tr>
<tr>
<th>
Cancelable

</th>
<td>
No

</td>
</tr>
<tr>
<th>
Default action

</th>
<td>
 ?

</td>
</tr>
</table>
## Examples

The following script queries the event [**target**](/dom/Event/target) as the text in a **textArea** is changed.

``` js
<script type="text/javascript">
function handleInput(ev) {
    alert(ev.target.value);
}
window.onload = function() {
    document.getElementById('myTextArea').addEventListener('input',handleInput,false);
}
</script>
<textarea id="myTextArea">Edit this text.</textarea>
```

## Notes

### Remarks

You can use the **oninput** to detect when the contents of a **textArea**, **input type=text**, or **input type=password** have changed. This event occurs immediately after modification, unlike the [**change**](/dom/Element/change) event, which occurs when the element loses focus. To invoke this event, do one of the following:

-   Enter some text into a form field.
-   Cut, delete, or paste content.
-   Navigate to another document.

### Syntax

### Standards information

-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374)

## See also

### External resources

-   [DOM Level 2](http://www.w3.org/TR/2003/REC-DOM-Level-2-HTML-20030109/html.html#ID-6043025)
