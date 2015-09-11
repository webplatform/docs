---
title: querySelectorAll
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs example, remove topic cluster flags'
readiness: 'Almost Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Element
    href: /dom/Element
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /dom/Element
standardization_status: 'W3C Working Draft'
summary: 'Returns a list of elements that match a provided selector.'
tags:
  - API
  - Object
  - Methods
  - DOM
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - selection
uri: 'css/selectors api/querySelectorAll'

---
## <span>Summary</span>

Returns a list of elements that match a provided selector.

Method of [dom/Element](/dom/Element)[dom/Element](/dom/Element)

## <span>Syntax</span>

``` js
var elementList = element.querySelectorAll(/* see parameter list */);
```

## <span>Parameters</span>

### <span>selector</span>

 Data-type
:   String

 A selector or multiple selectors (separated by commas).

## <span>Return Value</span>

Returns an object of type DOM NodeDOM Node

A collection of DOM element nodes. The collection may be empty.

**Needs Examples**: This section should include examples.

## <span>Notes</span>

This method differs from the [**querySelector**](/css/selectors_api/querySelector) method by returning a collection of DOM element nodes that match the selector string, rather than only the first element found. Calling this method with an unknown selector (due to the browser not implementing it, or due to typo and such) may throw an exception.

## <span>Related specifications</span>

[Selectors API Level 1](http://www.w3.org/TR/selectors-api/)
:   Proposed Recommendation

## <span>See also</span>

### <span>Related articles</span>

#### <span>Selectors</span>

-   **querySelectorAll**

-   [ID](/css/selectors/ID)

-   [Namespaced](/css/selectors/Namespaced)

-   [Universal](/css/selectors/Universal)

-   [equality](/css/selectors/attributes/equality)

-   [Attribute selector](/css/selectors/attributes/existence)

-   [hyphen](/css/selectors/attributes/hyphen)

-   [prefix](/css/selectors/attributes/prefix)

-   [substring](/css/selectors/attributes/substring)

-   [suffix](/css/selectors/attributes/suffix)

-   [whitespace](/css/selectors/attributes/whitespace)

-   [:-ms-input-placeholder](/css/selectors/pseudo-classes/:-ms-input-placeholder)

-   [:checked](/css/selectors/pseudo-classes/:checked)

-   [:disabled](/css/selectors/pseudo-classes/:disabled)

-   [:empty](/css/selectors/pseudo-classes/:empty)

-   [:enabled](/css/selectors/pseudo-classes/:enabled)

-   [:first-child](/css/selectors/pseudo-classes/:first-child)

-   [:first-of-type](/css/selectors/pseudo-classes/:first-of-type)

-   [:focus](/css/selectors/pseudo-classes/:focus)

-   [:in-range](/css/selectors/pseudo-classes/:in-range)

-   [:indeterminate](/css/selectors/pseudo-classes/:indeterminate)

-   [:invalid](/css/selectors/pseudo-classes/:invalid)

-   [:lang(c)](/css/selectors/pseudo-classes/:lang(c))

-   [:last-of-type](/css/selectors/pseudo-classes/:last-of-type)

-   [:nth-child(n)](/css/selectors/pseudo-classes/:nth-child(n))

-   [:nth-last-child(n)](/css/selectors/pseudo-classes/:nth-last-child(n))

-   [:nth-last-of-type(n)](/css/selectors/pseudo-classes/:nth-last-of-type(n))

-   [:nth-of-type(n)](/css/selectors/pseudo-classes/:nth-of-type(n))

-   [:only-child](/css/selectors/pseudo-classes/:only-child)

-   [:only-of-type](/css/selectors/pseudo-classes/:only-of-type)

-   [:optional](/css/selectors/pseudo-classes/:optional)

-   [:required](/css/selectors/pseudo-classes/:required)

-   [:root](/css/selectors/pseudo-classes/:root)

-   [:target](/css/selectors/pseudo-classes/:target)

-   [:valid](/css/selectors/pseudo-classes/:valid)

-   [::selection](/w/index.php?title=selection&action=edit&redlink=1)

-   [type](/css/selectors/type)

### <span>Related pages (MSDN)</span>

-   `Document`
-   `a`
-   `address`
-   `b`
-   `big`
-   `blockQuote`
-   `body`
-   `button`
-   `caption`
-   `center`
-   `cite`
-   `code`
-   `col`
-   `colGroup`
-   `dd`
-   `dfn`
-   `dir`
-   `div`
-   `dl`
-   `dt`
-   `em`
-   `fieldSet`
-   `form`
-   `hn`
-   `html`
-   `i`
-   `img`
-   `input type=button`
-   `input type=checkbox`
-   `input type=file`
-   `input type=image`
-   `input type=password`
-   `input type=radio`
-   `input type=reset`
-   `input type=submit`
-   `input type=text`
-   `isIndex`
-   `kbd`
-   `label`
-   `legend`
-   `li`
-   `listing`
-   `marquee`
-   `menu`
-   `noBR`
-   `ol`
-   `p`
-   `plainText`
-   `pre`
-   `s`
-   `samp`
-   `small`
-   `span`
-   `strike`
-   `strong`
-   `sub`
-   `sup`
-   `table`
-   `tBody`
-   `td`
-   `textArea`
-   `tFoot`
-   `th`
-   `tHead`
-   `tr`
-   `tt`
-   `u`
-   `ul`
-   `var`
-   `xmp`
-   `Reference`
-   `querySelector`
-   `IElementSelector`
-   `Other Resources`
-   `W3C Selectors API`
-   `W3C Selectors`
