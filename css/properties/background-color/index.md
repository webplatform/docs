---
title: background-color
code_samples:
  - 'http://chrisdavidmills.github.com/simple-background-color/'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`transparent`'
  'Applies to': 'All elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'the computed color'
  Animatable: 'Yes'
  '[CSS Object Model Property](/css/concepts/cssom)': '`backgroundColor`'
  Percentages: N/A
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Sets a color to fill up the background of an element it is applied to and accepts any valid CSS color.'
tags:
  - CSS
  - Properties
uri: css/properties/background-color

---
## Summary

Sets a color to fill up the background of an element it is applied to and accepts any valid CSS color.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `transparent`

Applies to
:   All elements

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   the computed color

Animatable
:   Yes

[CSS Object Model Property](/css/concepts/cssom)
:   `backgroundColor`

Percentages
:   N/A

## Syntax

-   `background-color: color`
-   `background-color: inherit`
-   `background-color: transparent`

## Values

transparent
:   The default value; you will be able to see the elements behind the element in question showing through it.

color
:   `background-color` accepts a single color as its value, which can be a keyword, hex, RGB, RGBa, HSL or HSLa color value. See the [CSS color values](/css/color) page for more details.

inherit
:   The element's background-color is inherited from its parent element.

## Examples

The HTML for this example is a series of simple div elements. Each one has the color information applied to it written inside it for ease of reference.

``` html
<h2>Keywords</h2>

<div id="c1">
  <p><code>background-color: red;</code></p>
</div>

<div id="c2">
  <p><code>background-color: green;</code></p>
</div>

<div id="c3">
  <p><code>background-color: blue;</code></p>
</div>

<h2>Hex values</h2>

<div id="c4">
  <p><code>background-color: #ff0000;</code></p>
</div>

<div id="c5">
  <p><code>background-color: #008000;</code></p>
</div>

<div id="c6">
  <p><code>background-color: #0000ff;</code></p>
</div>

  etc.
```

The CSS then floats the divs next to one another and gives them the same basic look. After that, each block is given a different color value, to demonstrate how keywords, hex, RGB(a), HSL(a) and opacity affect them.

``` css
html {
  background: url(bg.png);
  font-family: sans-serif;
  font-size: 10px;
}

body {
  width: 1024px;
  margin: 0 auto;
}

p {
  color: white;
  text-shadow: 0 1px 1px black;
  padding: 10px;
  font-size: 1.4rem;
}

div {
  height: 75px;
  float: left;
  width: 32%;
  margin-right: 1%;
  box-shadow: 0px 0px 10px black;
}

h2 {
  clear: both;
  padding-top: 1.5rem;
}

#c1 {
  background-color: red;
}

#c2 {
  background-color: green;
}

#c3 {
  background-color: blue;
}

#c4 {
  background-color: #ff0000;
}

#c5 {
  background-color: #008000;
}

#c6 {
  background-color: #0000ff;
}

etc
```

[View live example](http://chrisdavidmills.github.com/simple-background-color/)

## Usage

     * A strongly contrasting combination of foreground and background color should be used to make sure your textual content is as readable as possible. To check whether your color contrast passes accessibility conformance criteria, you can use an online checker such as Lea Verou’s Contrast Ratio which accepts any valid CSS color.

-   When using a newer color value type such as RGBa, HSL or HSLa, be aware that older browsers such as IE6-8 don't support these, so you should provide a fallback colour value so that foreground text will still be readable, either in the same stylesheet, or hidden away behind a [conditional comment](http://dev.opera.com/articles/view/supporting-ie-with-conditional-comments/). So for example:

```
background-color: #ff0000;
background-color: rgba(255,0,0,0.6);
```

## Notes

Internet Explorer 8 & 9 suffer from a bug where elements with a computed **background-color** of `transparent` that are overlaid on top of other element(s) won't receive `click` events. Any `click` events will be fired at the underlying element(s) instead. See [this live example](http://jsfiddle.net/YUKma/show/) for a demonstration.

Known workarounds for this bug:

-   For IE9 only:
    -   Set `background-color: rgba(0,0,0,0)`
    -   Set [`opacity`](/css/properties/opacity)`: 0` and an explicit **background-color** other than `transparent`
-   For IE8 and IE9
    -   Set [`filter`](http://msdn.microsoft.com/en-us/library/ms532847(v=vs.85).aspx)`: alpha(opacity=0);` and an explicit **background-color** other than `transparent`

## Related specifications

[CSS Backgrounds & Borders Level 3](http://www.w3.org/TR/css3-background/#the-background-color)
:   W3C Candidate Recommendation

[CSS 2.1 Colors and backgrounds](http://www.w3.org/TR/CSS21/colors.html)
:   W3C Recommendation

## See also

### Related articles

#### Background

-   [background](/css/cssom/properties/background)

-   [background](/css/properties/background)

-   [background-attachment](/css/properties/background-attachment)

-   [background-blend-mode](/css/properties/background-blend-mode)

-   [background-clip](/css/properties/background-clip)

-   **background-color**

-   [background-image](/css/properties/background-image)

-   [background-origin](/css/properties/background-origin)

-   [background-position](/css/properties/background-position)

-   [background-position-x](/css/properties/background-position-x)

-   [background-position-y](/css/properties/background-position-y)

-   [background-repeat](/css/properties/background-repeat)

-   [background-size](/css/properties/background-size)

-   [JavaScript animation](/tutorials/animation_in_javascript_2)

### External resources

-   <http://dev.opera.com/articles/view/color-in-opera-10-hsl-rgb-and-alpha-transparency/>
