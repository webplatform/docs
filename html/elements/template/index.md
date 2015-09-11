---
title: template
attributions:
  - 'Portions of this content come from HTML5Rocks! [article](http://www.html5rocks.com/en/tutorials/webcomponents/template/)'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLTemplateElement](/w/index.php?title=dom/HTMLTemplateElement&action=edit&redlink=1)'
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Templates allow you to declare fragments of markup which are parsed as HTML, go unused at page load, but can be instantiated later on at runtime.'
tags:
  - Markup
  - Elements
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/HTMLTemplateElement
uri: html/elements/template

---
## <span>Summary</span>

Templates allow you to declare fragments of markup which are parsed as HTML, go unused at page load, but can be instantiated later on at runtime.

## <span>Overview Table</span>

[DOM Interface](/dom/interface)
:   [HTMLTemplateElement](/w/index.php?title=dom/HTMLTemplateElement&action=edit&redlink=1)

The content of a `<template>` element is a hidden portion of the DOM and does not render on page load: scripts don't run, text or images don't display, audio doesn't play, and so forth. Neither are the child nodes of the `<template>` accessible with the JavaScript `getElementbyId()` or `querySelector()` methods.

Templates can be placed anywhere inside of the `<head>`, `<body>`, and `<frameset>` elements; It can also be used as a child of a `<table>` or a `<select>` element.

## <span>Examples</span>

### <span>Basic example</span>

``` html


<table>
<tr>
  <template id="cells-to-repeat">
    <td>some content</td>
  </template>
</tr>
</table>
```

</pre>

To use a template, you need to activate it. Otherwise its content will not render. The simplest way to do this is by creating a deep copy of its `.content `using `cloneNode()`. The `.content` property is read-only and references a `DocumentFragment` containing the guts of a template.

``` js
var t = document.querySelector('#mytemplate');
t.content.querySelector('img').src = 'logo.png'; // Populate the src at runtime.
document.body.appendChild(t.content.cloneNode(true));
```

### <span>Shadow DOM example</span>

But the more interesting use of the `<template>` tag is in concert with the Shadow DOM and the `<content>` tag. Use the Shadow DOM to achieve an encapsulation of the presentation (style) of the element and the `<content>` tag to provide separation of content from the element. The element (shadow host) is implemented with a `<template>` that encapsulates the styles, thereby providing a boiler plate, and a `<content>` tag, thereby providing for the reuse of the template for different content.

``` html


<template id="nameTagTemplate">
<style>
  …
</style>
<div class="outer">
  <div class="boilerplate">
    Hi! My name is
  </div>
  <div class="name">
    <content></content>
  </div>
</div>
</template>

<div id="nameTag"></div>
```

</pre>

Now all you have to do to stamp out the element is run your template through the ShadowRoot.

``` js
var shadow = document.querySelector('#nameTag').webkitCreateShadowRoot();
var template = document.querySelector('#nameTagTemplate');
document.querySelector('#nameTag').textContent = 'Shellie';
shadow.appendChild(template.content);
template.remove();
```

## <span>Usage</span>

     The template contents are hidden implicitly since they are not part of the document. The template element itself must be hidden through the user agent style sheet, as in the following:

``` css
@namespace "http://www.w3.org/1999/xhtml";

template {
    display : none;
}
```

## <span>Notes</span>

-   If you're using [modpagespeed](https://code.google.com/p/modpagespeed/), be careful of this [bug](http://code.google.com/p/modpagespeed/issues/detail?id=625). Templates that define inline `<style scoped>`, many be moved to the `head` with PageSpeed's CSS rewriting rules.
-   There's no way to "prerender" a template, meaning you cannot preload assets, process JS, download initial CSS, etc. That goes for both server and client. The only time a template renders is when it goes live.
-   Be careful with nested templates. They don't behave as you might expect, and nested templates must be activated separately.

## <span>Related specifications</span>

[HTML 5.1](http://www.w3.org/TR/html51/semantics.html#the-template-element)
:   W3C Working Draft

[HTML 5](http://www.w3.org/TR/html5/scripting-1.html#the-template-element)
:   W3C Recommendation

## <span>See also</span>

### <span>Related articles</span>

#### <span>Web Components</span>

-   [register](/dom/Document/register)

-   [shadowdom](/dom/shadowdom)

-   [is](/html/attributes/is)

-   [reset-style-inheritance](/html/attributes/reset-style-inheritance)

-   [content](/html/elements/content)

-   [element](/html/elements/element)

-   **template**

### <span>External resources</span>

-   [HTML's New Template Tag](http://www.html5rocks.com/en/tutorials/webcomponents/template/)
-   [Shadow DOM 101](http://www.html5rocks.com/en/tutorials/webcomponents/shadowdom/)
