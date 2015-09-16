---
title: Option
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
relationships:
  subclass_of:
    predicate: 'Inherits from '
    value: HTMLOptionElement
    href: /dom/HTMLOptionElement
tags:
  - API
  - Objects
  - DOM
uri: dom/Option

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Inherits from [HTMLOptionElement](/dom/HTMLOptionElement)[HTMLOptionElement](/dom/HTMLOptionElement)

## Properties

*No properties.*

## Methods

*No methods.*

## Events

*No events.*

## Inherited from HTMLOptionElement

### Properties

API Name
:   Summary

[defaultSelected](/dom/HTMLOptionElement/defaultSelected)
:   Gets or sets the value of the [selected](/html/attributes/selected) HTML attribute.

### Methods

*No methods.*

### Events

*No events.*

## Examples

The following script creates three new **option** objects and adds them to a **select** element. Because of the optional arguments, option "Two" is originally selected but option "Three" gains focus when the reset button is pressed.

``` html
<form action="#">
<select id="oSelect"></select>
<button type="reset">Reset to Defaults</button>
</form>
<script type="text/javascript">
var sel = document.getElementById('oSelect');
sel.options.add( new Option("One","1") );
sel.options.add( new Option("Two","2",false,true) );
sel.options.add( new Option("Three",3,1,0) );
</script>
```

## Notes

Use this object to instantiate new **option** elements before adding them to a **select** element. You can specify up to four optional arguments:

||
|sText|**String** that specifies the option text.|
|sValue|**String** that specifies the option value.|
|bDefaultSelected|**Boolean** that indicates whether the option is the default selection.|
|bSelected|**Boolean** that indicates whether this option is selected when it is added to the collection.|

  Numeric values are coerced into string and Boolean equivalents if possible.

## Related specifications

[WHATG HTML](http://www.whatwg.org/specs/web-apps/current-work/multipage/forms.html#the-option-element)
:   Living Standard

[HTML5](http://www.w3.org/TR/html5/forms.html#the-option-element)
:   Last Call Working Draft
