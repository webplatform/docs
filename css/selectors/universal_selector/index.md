---
title: universal selector
tags:
  - CSS
uri: 'css/selectors/universal selector'

---
The *universal selector*, written as a CSS qualified name [CSS3NAMESPACE](http://www.w3.org/TR/2011/REC-css3-selectors-20110929/#CSS3NAMESPACE) with an asterisk (\* U+002A) as the local name, represents the qualified name of any element type. It represents any single element in the document tree in any namespace (including those without a namespace) if no default namespace has been specified for selectors. If a default namespace has been specified, see Universal selector and Namespaces below.

If a universal selector represented by \* (i.e. without a namespace prefix) is not the only component of a sequence of simple selectors selectors or is immediately followed by a pseudo-element, then the \* may be omitted and the universal selector's presence implied.

``

    Examples:

    *[hreflang|=en] and [hreflang|=en] are equivalent,

    *.warning and .warning are equivalent,

    *#myid and #myid are equivalent.

</code>

**Note**: it is recommended that the \* not be omitted, because it decreases the potential confusion between, for example, *div :first-child* and *div:first-child*. Here, *div \*:first-child* is more readable.

## Universal selector and namespaces

The universal selector allows an optional namespace component. It is used as follows:

``

    ns|* all elements in namespace ns

    *|* all elements

    |* all elements without a namespace

    * if no default namespace has been specified, this is equivalent to *|*. Otherwise it is equivalent to ns|* where ns is the default namespace.

</code>

A universal selector containing a namespace prefix that has not been previously declared is an invalid selector.