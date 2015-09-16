---
title: register
attributions:
  - 'Portions of this content come from HTML5Rocks! [article](http://www.html5rocks.com/en/tutorials/webcomponents/customelements/)'
notes:
  - 'Needs compat tables and better spec links'
readiness: 'Almost Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Document
    href: /dom/Document
  return_type:
    predicate: 'Returns an object of type  '
    value: Object
    href: /dom/Document
standardization_status: 'W3C Editor''s Draft'
summary: 'Registers a new, custom element and returns the element''s constructor.'
tags:
  0: API
  1: Object
  2: Methods
  4: DOM
uri: dom/Document/register

---
## Summary

Registers a new, custom element and returns the element's constructor.

Method of [dom/Document](/dom/Document)[dom/Document](/dom/Document)

## Syntax

``` js
var XFoo = document.register(/* see parameter list */);
```

## Parameters

### type

 Data-type
:   String

 The custom element's tag name. The name must contain a dash (-). So for example, \<x-foo\>, \<foo-element\>, and \<my-foo-element\> are valid names, while \<tabs\> and \<foo\_bar\> are not.

### options

 Data-type
:   Object

(Optional)

The object describing the element's prototype, public properties and methods.

## Return Value

Returns an object of type ObjectObject

## Examples

Register's the custom element and adds it to the DOM.

``` js
var XFoo = document.register('x-foo');
document.body.appendChild(new XFoo());
```

Registers the custom element and defines the element's prototype.

``` js
var XFoo = document.register('x-foo', {
  prototype: Object.create(HTMLElement.prototype, {
    bar: {
      get: function() { return 5; }
    },
    foo: {
      value: function() {
        alert('foo() called');
      }
    }
  })
});
```

## Notes

The custom element name must not be one of the following existing hyphen-containing element names:

-   annotation-xml
-   color-profile
-   font-face
-   font-face-src
-   font-face-uri
-   font-face-format
-   font-face-name
-   missing-glyph

## Related specifications

[Custom Elements](https://dvcs.w3.org/hg/webcomponents/raw-file/tip/spec/custom/index.html)
:

## See also

### Related articles

#### Web Components

-   **register**

-   [shadowdom](/dom/shadowdom)

-   [is](/html/attributes/is)

-   [reset-style-inheritance](/html/attributes/reset-style-inheritance)

-   [content](/html/elements/content)

-   [element](/html/elements/element)

-   [template](/html/elements/template)

### External resources

-   [Custom Elements](http://www.html5rocks.com/en/tutorials/webcomponents/customelements/) on [HTML5Rocks!](http://www.html5rocks.com)
