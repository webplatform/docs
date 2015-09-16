---
title: list-style-type
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/CSS/list-style-type)'
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  0: 'http://gist.github.com/6798718'
  2: 'http://gist.github.com/5597602'
  3: 'http://gist.github.com/5598129'
  4: 'http://gist.github.com/5597530'
  5: 'http://gist.github.com/5697355'
notes:
  - 'Add specification, complete compatibility.'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`disc`'
  'Applies to': 'elements with ''display: list-item'''
  '[Inherited](/css/concepts/inherited)': 'Yes'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'as specified'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
readiness: 'In Progress'
summary: 'Specifies the type of list-item marker in a list.'
tags:
  - CSS
  - Properties
uri: css/properties/list-style-type

---
## Summary

Specifies the type of list-item marker in a list.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `disc`

Applies to
:   elements with 'display: list-item'

[Inherited](/css/concepts/inherited)
:   Yes

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   as specified

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:

## Syntax

-   `list-style-type: armenian`
-   `list-style-type: circle`
-   `list-style-type: decimal`
-   `list-style-type: decimal-leading-zero`
-   `list-style-type: disc`
-   `list-style-type: georgian`
-   `list-style-type: inherit`
-   `list-style-type: lower-alpha`
-   `list-style-type: lower-greek`
-   `list-style-type: lower-latin`
-   `list-style-type: lower-roman`
-   `list-style-type: none`
-   `list-style-type: square`
-   `list-style-type: upper-alpha`
-   `list-style-type: upper-latin`
-   `list-style-type: upper-roman`

## Values

armenian
:   The marker is traditional Armenian numbering

circle
:   circle

decimal
:   number. This is default for \<ol\>

decimal-leading-zero
:   number with leading zeros (01, 02, 03, etc.)

disc
:   filled circle. This is default for \<ul\>

georgian
:   traditional Georgian numbering

inherit
:   The value of the listStyleType property is inherited from parent element

lower-alpha
:   lower-alpha (a, b, c, d, e, etc.)

lower-greek
:   lower-greek

lower-latin
:   lower-latin (a, b, c, d, e, etc.)

lower-roman
:   lower-roman (i, ii, iii, iv, v, etc.)

none
:   No marker is shown

square
:   square

upper-alpha
:   upper-alpha (A, B, C, D, E, etc.)

upper-latin
:   upper-latin (A, B, C, D, E, etc.)

upper-roman
:   upper-roman (I, II, III, IV, V, etc.)

## Examples

The following examples use the **`list-style-type`** attribute and the **`list-style-type`** property to set the markers.

This example uses **`ul`** as a selector in an embedded (global) style sheet to change the marker type to **`circle`**.

``` css
<style>
    ul { list-style-type:circle }
</style>
```

[View live example](http://code.webplatform.org/gist/6798718)

This example demonstrates the use of `decimal-leading-zero`.

``` html
<style type="text/css">
.decleadzero {
    list-style-type: decimal-leading-zero;
}
...
</style>
<body>
 <ol class="decleadzero">
  <li>This is the first item. </li>
  <li>This is the second item. </li>
  <li>This is the third item. </li>
 </ol>
    ...
</body>
```

[View live example](http://code.webplatform.org/gist/6798718)

Using the `list-style-type` on ordered lists

``` css
/**
 * using list-style-type on ordered lists
 * the default for ol's is list-style-type: decimal
 */

.list-style--leading-zero {
    list-style-type:  decimal-leading-zero;
}

.list-style--roman {
    list-style-type:  upper-roman; /* you can also use lower-roman */
}
```

[View live example](http://code.webplatform.org/gist/5597602)

If the left padding of a line item is set to 0 and the list has `list-style-position: outside;` (which is the default) the list-item markers will not show.

``` css
/*
If the left padding is set to 0 the list-item markers do not show
This happens only if the list-style-position is set on outside (which is the default)
*/

ul {
    padding:0;
}

.list-position--inside {
    list-style-position: inside;
}
```

[View live example](http://code.webplatform.org/gist/5598129)

Example for unordered lists

``` css
/*
    Example for unordered lists
*/

.list-style--circle {
    list-style-type: circle;
}

.list-style--square {
    list-style-type: square;
}

.list-style--square {
    list-style-type: none; /* use none to remove the bullets */
}
```

[View live example](http://code.webplatform.org/gist/5597530)

Example for unordered lists with `list-style-type` set as `none` which removes the default bullet style of the unordered list.

``` css
/**
 * Example of list-style-type

 One value for the list-style-type is none which just removes the bullets and all.
 This example includes two unordered lists one with list-style-type set as none and other set as square bullets.
 */

#withBullets ul {
    color: #f06;
    font: italic 100% Georgia, serif;
    width: 500px;
    padding:10px;
    margin:10px;
    list-style-type:none;   /*To remove the default bullet style*/
}
#withBullets li{
    display:inline;
    margin:8px;
    padding:4px;
}
#withBullets li:hover{
    border-bottom:3px solid black;
    border-radius:4px;
}

ul{
    color: #f06;
    font: italic 100% Georgia, serif;
    width: 500px;
    padding:10px;
    margin:10px;
    list-style-type:square;
}
li{
    margin:8px;
}
a:link{text-decoration:none;color:green;}
a:hover{text-decoration:none;color:green;}
a:active{text-decoration:none;color:green;}
a:visited{text-decoration:none;color:green;}
```

[View live example](http://code.webplatform.org/gist/5697355)

## Usage

     The list-style-type CSS property specifies appearance of a list item element. As it is the only one who defaults to display:list-item, this is usually a <li> element, but can be any element with this display value.

## Notes

### Notes

-   The color of the marker will be the same as the computed color of the element it applies to.

-   Some `list-style-type`s require a suitable font installed to display as expected.

-   The CSS specification does not define how alphabetic systems wrap at the end of the alphabet. For instance, after 26 list items, upper-alpha rendering is undefined. Firefox and other browsers will continue as AA, AB, AC,... For long lists, it is recommended that authors specify true numbers.

-   The list styles `hebrew`, `cjk-ideographs`, `hiragana`, `katakana`, `hiragana-iroha` and `katakana-iroha` were specified in CSS2 but removed from CSS 2.1 due to lack of implementation experience. They are expected to return in the CSS3 Lists module.

-   The property also supports a shorthand syntax which is list-style

-   If the left padding of a list is set to 0 using one of the padding properties, the list-item markers do not show only if that list has the default list-style-position: inside; . For a better understanding see the examples.

## See also

### Related articles

#### Generated and Replaced Content

-   [Generated and Replaced Content](/css/generated_and_replaced_content)

-   [content](/css/properties/content)

-   [counter-increment](/css/properties/counter-increment)

-   [counter-reset](/css/properties/counter-reset)

-   [list-style-image](/css/properties/list-style-image)

-   **list-style-type**

-   [object-fit](/css/properties/object-fit)

### Related pages

-   `CSSStyleDeclaration`
-   `currentStyle`
-   `runtimeStyle`
-   `style`
