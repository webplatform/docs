---
title: :target
tags:
  - CSS
  - Selectors
readiness: 'Not Ready'
notes:
  - 'No matching spec'
summary: 'The :target pseudo-class (note the ":") represents an element in the current document, if any, that has id attribute set to a name that is matching the fragment identifier of the current URI.'
code_samples:
  - 'http://gist.github.com/6f2803eda8ad3c66aaf4'
uri: 'CSS/Selectors/pseudo-classes/:target'

---
# :target pseudo-class selector

## Summary

The :target pseudo-class (note the ":") represents an element in the current document, if any, that has id attribute set to a name that is matching the fragment identifier of the current URI.

 An URI fragment is what follows the "number sign" (`#`).

![example-css-target-pseudo-activated.png](/assets/public/e/e6/example-css-target-pseudo-activated.png)

URIs with fragment identifier can be used to link to a specific part of a document, known as the target element. This also how we can navigate directly to a section of a page long without scrolling manually.

Scrolling automatically to a fragment is not the only benefit; It is also possible to target and style those elements through CSS.

Let us say you have a section in a document called "`foo`" (e.g. `<div id="foo">...</div>`), and you want to style it differently when it gets linked. When somebody navigates to that page with the appropriate URI fragment in the address bar (e.g. `http://example.com/some/page.html#foo`) we then can adjust the style to suit our requirements.

Any element can be a target, as long as it has the `id=".."` attribute set, and the current URI matches it. To use the selector, we use the `:target` pseudo-class notation. If the document's URI has no fragment identifier, then the document has no target element.

## Using the selector

To use the selector, append the pseudo selector (`:target`) after a selector string.

``` {.css}
  .note:target { /* ... */ }
```

 In this example, the selector targets an element that has a [*class name* selector](/css/selectors/class) `note` and will be used when its matching elements also has an `id` attribute matching the current URI.

Since it is a pseudo selector, it has to be at the end of the chain (e.g. `tagName#idName.className:pseudo-selector`).

For example, to change the background color of ANY tag that happens to be refered in the URI, you can do like the following:

``` {.css}
*:target { background-color: red }
```

## Examples

Changing background color of an element that has an id attribute with a name that matches the current URI after the pound (\#)

``` {.css}
*:target {
  background-color: #f06;
 /* any element that has an id attribute matching
    in the URI will have the background color
    affected to pink */
}
```

[View live example](http://code.webplatform.org/gist/6f2803eda8ad3c66aaf4)

## Notes

The `id` attribute was new in HTML 4 (December 1997). Before that, we were using the name attribute in an ahcnor tag (e.g. \<a name="foo"\>. The `:target` pseudo-class applies to those targets as well.

## See also

### Related articles

#### Pseudo-Classes

-   **:target pseudo-class selector**

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

