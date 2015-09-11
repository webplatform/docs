---
title: Namespaced
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs title, summary, spec reference, standardization status, remove topic cluster flags'
readiness: 'In Progress'
tags:
  - CSS
  - Selectors
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - selection
uri: css/selectors/Namespaced

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

## <span>Examples</span>

**Type** selectors allow an optional namespace component (namespace prefix). The namespace prefix can be left empty to indicate that the selector is only to match elements with no namespace, or an asterisk can be used to indicate that the selector matches elements in any namespace (as well as elements with no namespace).

``` html
@namespace myprfx url(http://www.microsoft.com);
```

[First, declare the namespace prefix (`myprfx` in this example): View live example]

## <span>Notes</span>

### <span>Remarks</span>

A *CSS qualified name* is an element or attribute name that is located within a namespace. To form a qualified name, first declare a namespace prefix by using the [**@namespace**](/css/atrules/@namespace) at-rule. Then, prepend the namespace prefix to the element or attribute name, separating the prefix and the name with a vertical bar (|). **Type**, universal, and attribute selectors can be namespaced, as shown in Examples.

### <span>Syntax</span>

`<strong/>prfx|selector {...}`

### <span>Parameters</span>

*prfx*
:   A namespace prefix. The namespace prefix is declared by the [**@namespace**](/css/atrules/@namespace) at-rule.
*selector*
:   A local element or attribute name.

### <span>Standards information</span>

-   [CSS Namespaces Module](http://go.microsoft.com/fwlink/p/?linkid=199777), Section 4

## <span>See also</span>

### <span>Related articles</span>

#### <span>Selectors</span>

-   [querySelectorAll](/css/selectors_api/querySelectorAll)

-   [ID](/css/selectors/ID)

-   **Namespaced**

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
