---
title: toString
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Range.toString](https://developer.mozilla.org/en-US/docs/Web/API/Range.toString) Article]'
  - 'Microsoft Developer Network: [[toString Method](http://msdn.microsoft.com/en-us/library/ie/hh869616(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Range
    href: /dom/Range
  return_type:
    predicate: 'Returns an object of type  '
    value: String
    href: /dom/Range
standardization_status: 'W3C Recommendation'
summary: 'Returns the contents of a Range as a string. This string contains only the data characters, no markup.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/Range/toString

---
## <span>Summary</span>

Returns the contents of a Range as a string. This string contains only the data characters, no markup.

Method of [dom/Range](/dom/Range)[dom/Range](/dom/Range)

## <span>Syntax</span>

``` js
var text = range.toString();
```

## <span>Return Value</span>

Returns an object of type StringString

Contains only the data characters, no markup.

## <span>Examples</span>

``` js
var range = document.createRange();

range.selectNode(document.getElementsByTagName("div").item(0));
text = range.toString();
```

### <span>Syntax</span>

text = range.toString();

### <span>Standards information</span>

-   [Document Object Model (DOM) Level 2 Traversal and Range Specification](http://go.microsoft.com/fwlink/p/?linkid=182712), Section 2.13

## <span>Related specifications</span>

[DOM](http://dom.spec.whatwg.org/#dom-range-stringifier)
:   Living Standard
