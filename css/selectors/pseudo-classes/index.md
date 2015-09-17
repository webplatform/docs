---
title: 'pseudo-classes'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/CSS/Pseudo-classes)'
notes:
  - 'Needs spec reference, standardization status'
readiness: 'Almost Ready'
summary: 'Dynamic pseudo-classes classify elements on characteristics other than their name, attributes, or content, in principle characteristics that cannot be deduced from the document tree.'
tags:
  - API_Listings
  - CSS
uri: css/selectors/pseudo-classes

---
## Summary

Dynamic pseudo-classes classify elements on characteristics other than their name, attributes, or content, in principle characteristics that cannot be deduced from the document tree.

|Page|Summary|
|:---|:------|
|[:target pseudo-class selector](/CSS/Selectors/pseudo-classes/:target)|The `:target` pseudo-class (note the ":") represents an element in the current document, if any, that has id attribute set to a name that is matching the fragment identifier of the current URI.|
|[:-ms-input-placeholder](/css/selectors/pseudo-classes/:-ms-input-placeholder)||
|[:checked](/css/selectors/pseudo-classes/:checked)|The **:checked** selector applies to toggable elements (e.g. radio buttons or checkboxes) that are toggled on.|
|[:disabled](/css/selectors/pseudo-classes/:disabled)||
|[:empty](/css/selectors/pseudo-classes/:empty)||
|[:enabled](/css/selectors/pseudo-classes/:enabled)||
|[:first-child](/css/selectors/pseudo-classes/:first-child)|The :first-child pseudo-class matches an element that is the first child element of some other element.|
|[:first-of-type](/css/selectors/pseudo-classes/:first-of-type)||
|[:focus](/css/selectors/pseudo-classes/:focus)|The **:focus** pseudo-class applies while an element has the focus, i.e. accepts keyboard or mouse events, or other forms of input.|
|[:in-range](/css/selectors/pseudo-classes/:in-range)|The `:in-range` pseudo selector selects input elements when their value is within a specified range.|
|[:indeterminate](/css/selectors/pseudo-classes/:indeterminate)||
|[:invalid](/css/selectors/pseudo-classes/:invalid)||
|[:lang(c)](/css/selectors/pseudo-classes/:lang(c))|The **:lang(c)** pseudo selector applies to documents that specifies the `lang` attribute to an HTML element. This allows to style based on which language (and/or dialect) a given section is written into.|
|[:last-of-type](/css/selectors/pseudo-classes/:last-of-type)||
|[:nth-child(n)](/css/selectors/pseudo-classes/:nth-child(n))||
|[:nth-last-child(n)](/css/selectors/pseudo-classes/:nth-last-child(n))||
|[:nth-last-of-type(n)](/css/selectors/pseudo-classes/:nth-last-of-type(n))||
|[:nth-of-type(n)](/css/selectors/pseudo-classes/:nth-of-type(n))||
|[:only-child](/css/selectors/pseudo-classes/:only-child)||
|[:only-of-type](/css/selectors/pseudo-classes/:only-of-type)||
|[:optional](/css/selectors/pseudo-classes/:optional)||
|[:required](/css/selectors/pseudo-classes/:required)||
|[:root](/css/selectors/pseudo-classes/:root)||
|[:valid](/css/selectors/pseudo-classes/:valid)||

## Usage

     A CSS pseudo-class is a keyword added to selectors that specifies a special state of the element to be selected. For example :hover will apply a style when the user hovers over the element specified by the selector.

Pseudo-classes, together with pseudo-elements, let you apply a style to an element not only in relation to the content of the document tree, but also in relation to external factors like the history of the navigator (`:visited`, for example), the status of its content (like `:checked` on some form elements), or the position of the mouse (like `:hover` which lets you know if the mouse is over an element or not).

## Examples

``` css
/* unvisited links */
a:link
/* visited links */
a:visited
/* user hovers */
a:hover
/* active links */
a:active
```

 An example of combining dynamic pseudo-classes:

``` css
a:focus
a:focus:hover
```

 The last selector matches `a` elements that are in the pseudo-class `:focus` and in the pseudo-class `:hover`.

> **Note:** An element can be both ‘`:visited`’ and ‘`:active`’ (or ‘`:link`’ and ‘`:active`’).
