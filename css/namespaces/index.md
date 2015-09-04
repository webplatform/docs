---
title: namespaces
tags:
  - CSS
uri: css/namespaces
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - CSS/Selectors

---
CSS Namespaces module defines syntax for using namespaces in CSS. It defines the `@namespace` rule for declaring a default namespace and for binding namespaces to namespace prefixes. It also defines a syntax for using those prefixes to represent namespace-qualified names. It does not define where such names are valid or what they mean: that depends on their context and is defined by a host language, such as Selectors, that references the syntax defined in the CSS Namespaces module.

## @namespace

The @namespace at-rule declares a namespace prefix and associates it with a given namespace name (a string). This namespace prefix can then be used in namespace-qualified names such as the CSS qualified names defined below.

### Example A

This rule declares a default namespace [http://www.w3.org/1999/xhtml](http://www.w3.org/1999/xhtml) to be applied to names that have no explicit namespace component.

    @namespace "http://www.w3.org/1999/xhtml";

### Example B

This rule declares a namespace prefix svg that is used to apply the namespace [http://www.w3.org/2000/svg](http://www.w3.org/2000/svg) where the svg namespace prefix is used.

    @namespace svg "http://www.w3.org/2000/svg";

## See also

-   [Namespaces Module Specification](http://www.w3.org/TR/css3-namespace/CSS)
-   [CSS Educational Materials for Beginners](/css/tutorials)
-   [CSS Properties Reference](/css/properties)
-   [CSS Selectors Reference](/w/index.php?title=CSS/Selectors&action=edit&redlink=1)
