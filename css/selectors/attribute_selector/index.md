---
title: attribute selector
tags:
  - CSS
uri: 'css/selectors/attribute selector'

---
Selectors allow the representation of an element's attributes. When a selector is used as an expression to match against an element, attribute selectors must be considered to match an element if that element has an attribute that matches the attribute represented by the attribute selector.

The following attribute selectors exist:

-   Presence and value selectors:
    -   `[attributename]`
    -   `[attributename="val"]`
    -   `[attributename~="val"]`
    -   `[attributename|="val"]`
-   Substring matching selectors:
    -   `[attributename^="val"]`
    -   `[attributename$="val"]`
    -   `[attributename*="val"]`

## <span>Examples</span>

The following attribute selector represents an h1 element that carries the title attribute, whatever its value:

``` css
h1[title]
```

 In the following example, the selector represents a span element whose class attribute has exactly the value "example":

``` css
span[class="example"]
```

 Multiple attribute selectors can be used to represent several attributes of an element, or several conditions on the same attribute. Here, the selector represents a span element whose hello attribute has exactly the value "Cleveland" and whose goodbye attribute has exactly the value "Columbus":

``` css
span[hello="Cleveland"][goodbye="Columbus"]
```

 The following CSS rules illustrate the differences between "=" and "\~=". The first selector would match, for example, an a element with the value "copyright copyleft copyeditor" on a rel attribute. The second selector would only match an a element with an href attribute having the exact value "<http://www.w3.org/>".

``` css
a[rel~="copyright"] { ... }
a[href="http://www.w3.org/"] { ... }
```

 The following selector represents an a element whose hreflang attribute is exactly "fr".

``` css
a[hreflang=fr]
```

 The following selector represents an a element for which the value of the hreflang attribute begins with "en", including "en", "en-US", and "en-scouse":

``` css
a[hreflang|="en"]
```

 The following selectors represent a DIALOGUE element whenever it has one of two different values for an attribute character:

``` css
DIALOGUE[character=romeo]
DIALOGUE[character=juliet]
```

 The following selector represents an HTML object, referencing an image:

``` css
object[type^="image/"]
```

 The following selector represents an HTML anchor a with an href attribute whose value ends with ".html".

``` css
a[href$=".html"]
```

 The following selector represents an HTML paragraph with a title attribute whose value contains the substring "hello"

``` css
p[title*="hello"]
```