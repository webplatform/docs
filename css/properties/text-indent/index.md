---
title: 'text-indent'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/Web/CSS/text-indent)'
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/5842068'
  - 'http://gist.github.com/5658652'
compatibility:
  feature: text-indent
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`0`'
  'Applies to': 'Block, inline-block, and table cells'
  '[Inherited](/css/concepts/inherited)': 'Yes'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'percentage or absolute length'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`textIndent`'
  Percentages: 'refer to width of containing block'
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Specifies the amount of space horizontally that should be left on the first line of the text of an element. This horizontal spacing is at the beginning of the first line and is in respect to the left edge of the containing block box.'
tags:
  - CSS
  - Properties
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/events/click
    - dom/events/mouseover
uri: css/properties/text-indent

---
## Summary

Specifies the amount of space horizontally that should be left on the first line of the text of an element. This horizontal spacing is at the beginning of the first line and is in respect to the left edge of the containing block box.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `0`

Applies to
:   Block, inline-block, and table cells

[Inherited](/css/concepts/inherited)
:   Yes

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   percentage or absolute length

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:   `textIndent`

Percentages
:   refer to width of containing block

## Syntax

-   `text-indent: <length/percentage> each-line`
-   `text-indent: <length/percentage> each-line`
-   `text-indent: <length/percentage> hanging`
-   `text-indent: inherit`
-   `text-indent: length`
-   `text-indent: percentage`

## Values

length
:   Floating-point number, followed by an absolute units designator (cm, mm, in, pt, or pc) or a relative units designator (em, ex, or px).

percentage
:   Integer, followed by a percent sign (%). This value is a percentage of the width of the parent object.

inherit
:   Inherits the value from the cascade.

\<length/percentage\> each-line
:   This value can only be used in conjunction with a length or percentage value (`text-indent: 7px each-line;`). It will affect not only the first line of the block container but also any line that is after a forced line break. This does not have affect on soft wrap break.

Currently experimental in CSS Text Level 3

\<length/percentage\> hanging
:   This value can only be used in conjunction with a length or percentage value (`text-indent: 7px hanging;`). It inverts which lines are indented so that everything but the first formatted line is indented.

Currently an experimental feature.

\<length/percentage\> each-line
:   This value can only be used in conjunction with a length or percentage value (`text-indent: 7px each-line;`). It indents all lines in the element, not just the first line.

Currently an experimental feature.

## Examples

The following examples use the **text-indent** attribute and the **text-indent** property to indent the object's text.

This example uses calls to an embedded style sheet to change the indent on the text when a [**click**](/w/index.php?title=dom/events/click&action=edit&redlink=1) event occurs. The text was originally indented 2 centimeters using **div** as a selector in the style sheet.

``` css
/* Indenting a line by an absolute value. */
p:nth-child(1) {
    text-indent: 3em;
}

/* Indenting a line by an absolute value, but with the `hanging` keyword. */
p:nth-child(2) {
    text-indent: 3em hanging;
}

/* Indenting a line by a percentage (the width used is the distance from the beginning to the end of the line.) */
p:nth-child(3) {
    text-indent: 50%;
}
```

[View live example](http://code.webplatform.org/gist/5842068)

This example uses JavaScript to indent the text within the **div** when a [**mouseover**](/w/index.php?title=dom/events/mouseover&action=edit&redlink=1) event occurs.

``` html
<!DOCTYPE html>
<html>
 <head>
 <title>Example</title>
  <script>
function initialize() {
  var element = document.getElementById("example");
  element.addEventListener("mouseover", function () {
    this.style.textIndent = "2cm";
  }, false);
}
window.addEventListener("load", initialize, false);
  </script>
 </head>
 <body>
  <div id="example">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Proin condimentum malesuada quam, ut ullamcorper nunc posuere in. Duis ullamcorper fringilla lorem eget accumsan. Praesent neque ipsum, tincidunt eget aliquet sit amet, tempor eget felis. Duis nibh magna, vestibulum et molestie sed, porttitor vel tellus. Nunc suscipit justo ut magna imperdiet pharetra. Suspendisse potenti. Vivamus vestibulum, dui eu fermentum blandit, nunc dolor aliquet massa, non elementum arcu arcu ut risus. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Suspendisse tincidunt nibh at ipsum semper eu tempor nisi ornare. Nunc vestibulum elementum dapibus. Morbi pellentesque nulla non est adipiscing id commodo eros blandit. Suspendisse mauris tellus, auctor a sodales a, consequat nec diam.</div>
 </body>
</html>
```

[View live example](http://code.webplatform.org/gist/5658652)

## Usage

     It is important to note that the keyword options (each-line and hanging) are experimental features; exercise caution when using them, as there is no guarantee of cross-browser compatibility.

## Notes

The property can be negative. An indent is not inserted in the middle of an object that was broken by another object, such as **br** in HTML.

## Related specifications

[CSS Text Module Level 3](http://www.w3.org/TR/css3-text/)
:   Working Draft

[CSS 2.1](http://www.w3.org/TR/CSS2/)
:   Recommendation
