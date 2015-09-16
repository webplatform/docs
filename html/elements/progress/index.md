---
title: 'progress'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/6365491'
  - 'http://gist.github.com/6365520'
  - 'http://gist.github.com/6365564'
  - 'http://gist.github.com/6365909'
compatibility:
  feature: progress
  topic: html
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLProgressElement](/w/index.php?title=dom/HTMLProgressElement&action=edit&redlink=1)'
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'The HTML &lt;progress&gt; element represents the completion progress of a task.'
tags:
  - Markup
  - Elements
  - HTML
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/HTMLProgressElement
uri: html/elements/progress

---
## Summary

The HTML &lt;progress&gt; element represents the completion progress of a task.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLProgressElement](/w/index.php?title=dom/HTMLProgressElement&action=edit&redlink=1)

<table class="wikitable">
<tr>
<th style="vertical-align: top" id="permitted-contents">
Permitted contents

</th>
<td style="vertical-align: top; padding-top: 10px">
Phrasing content, but may not contain any `<progress>` elements itself.

</td>
</tr>
<tr>
<th id="permitted-parents">
Permitted parents

</th>
<td>
Any element that can contain phrasing content.

</td>
</tr>
<tr>
<th id="tag-omission">
Tag omission

</th>
<td>
A `<progress>` element must have both a start tag and an end tag.

</td>
</tr>
</table>
The HTML `<progress>` element is a number in the range zero to a maximum, giving the fraction of work that has so far been completed. The progress element is not the correct element to use for something that is just a gauge, as opposed to task progress. For instance, indicating disk space usage using progress would be inappropriate. Instead, the [meter](/html/elements/meter) element is available for such use cases.

The content of the **progress** element should represent the set min/max/value attributes in human readable form. This will be picked up by assistive technologies as well as act as a fallback for browsers not supporting the element.

### Attributes

This element supports the HTML5 [global attributes](/html/global_attributes).

value
:   How much of the task has been completed. If [max](#attribute-max) is not set, this should be a value between 0 and 1, if [max](#attribute-max) is set, this should be a value between 0 and [max](#attribute-max).
max
:   How much work the task requires in total. This is optional, if it's not set then [value](#attribute-value) is a percentage.

## Examples

Example of a basic progress element

``` html
<progress value="165" max="200">165 of 200 finished</progress>
```

[View live example](http://code.webplatform.org/gist/6365491)

Example of progress without a maximum

``` html
<progress value="0.72">72% done</progress>
```

[View live example](http://code.webplatform.org/gist/6365520)

Styling options for the progress bar (vendor-specific)

``` css
progress {
  -webkit-appearance: none;
}

progress::-webkit-progress-bar {
  background-color: lightgray;
}

progress::-webkit-progress-value {
  background-color: lightgreen;
}
```

[View live example](http://code.webplatform.org/gist/6365564)

Progress element without value

``` html
<progress></progress>
```

[View live example](http://code.webplatform.org/gist/6365909)

## Usage

     When the value attribute is omitted, the <progress> element becomes indeterminate, that is, it shows activity but not how much progress has actually been made.

## Related specifications

[HTML 5.1](http://www.w3.org/TR/html51/forms.html#the-progress-element)
:   W3C Working Draft

[HTML 5](http://www.w3.org/TR/html5/forms.html#the-progress-element)
:   W3C Recommendation

## See also

### Other articles

-   [HTML5 meter element](/html/elements/meter)
