---
title: reset-style-inheritance
tags:
  - Markup
  - Attributes
readiness: 'Not Ready'
standardization_status: 'W3C Working Draft'
notes:
  - "Deprecated; deletion candidate. See\nhttps://groups.google.com/forum/#!topic/polymer-dev/wmcncSDx_Jo"
summary: "Indicates whether the inheritable CSS properties are set to the initial value established at the shadow boundary.\n"
uri: html/attributes/reset-style-inheritance
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/apis/ShadowRoot/resetStyleInheritance

---
# reset-style-inheritance

## Summary

Indicates whether the inheritable CSS properties are set to the initial value established at the shadow boundary.

**Deprecated -- do not use**

Applies to
:   dom/HTMLContentElement

Read only. Indicates the state of the [resetStyleInheritance](/w/index.php?title=dom/apis/ShadowRoot/resetStyleInheritance&action=edit&redlink=1) flag for this insertion point. If present, the value of the flag must be set to true. Otherwise, the value must be set to false. If true, the inheritable CSS properties are set to the initial value at the shadow boundary. If false (default value), the properties continue to inherit.

**Needs Examples**: This section should include examples.

## See also

### Related articles

#### Web Components

-   [register](/dom/Document/register)

-   [shadowdom](/dom/shadowdom)

-   [ShadowRoot](/dom/shadowdom/ShadowRoot)

-   [is](/html/attributes/is)

-   **reset-style-inheritance**

-   [content](/html/elements/content)

-   [element](/html/elements/element)

-   [template](/html/elements/template)

