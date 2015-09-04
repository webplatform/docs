---
title: main
tags:
  - Markup
  - Elements
  - HTML
readiness: 'In Progress'
standardization_status: 'W3C Editor''s Draft'
notes:
  - 'Add Category, Parent, Children and Compatibility information.'
summary: 'Represents the main content of the body of a document or application.'
uri: html/elements/main

---
# main

## Summary

Represents the main content of the body of a document or application.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLElement](/dom/HTMLElement)

## Examples

The following example shows a basic usage of the `<main>` element

``` {.html}
<!DOCTYPE html>
<html>
<head>
  <title>Main element example</title>
</head>
<body>
  <header>
    <h1>The main element</h1>
  </header>
  <main>
    <h2>Some content on the main element</h2>

    <article>
      ...
    </artice>
    <section>
      ...
    </section>
  </main>
  <footer>
    Copyright 2013 Web Platform
  </footer>
</body>
</html>
```

## Notes

-   It is advised to use ARIA `role="main"` attribute on the main element until browsers have implemented the element.

-   There must not be more than one `<main>` element in a document, and it must not be a descendent of an `<article>`, `<aside>`, `<footer>`, `<header>`, or `<nav>` element.

## Related specifications

Specification
:   Status
[HTML 5.1](http://www.w3.org/TR/html51/grouping-content.html#the-main-element)
:   W3C Working Draft
[HTML 5](http://www.w3.org/TR/html5/grouping-content.html#the-main-element)
:   W3C Recommendation

## See also

### Related articles

#### Document Structure

-   [button](/html/elements/button)

-   [button](/html/elements/button/ja)

-   [footer](/html/elements/footer)

-   [head](/html/elements/head)

-   **main**

-   [nav](/html/elements/nav)

-   [p](/html/elements/p)

-   [section](/html/elements/section)

