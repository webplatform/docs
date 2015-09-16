---
title: 'outline'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/).'
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  0: 'http://gist.github.com/5546931'
  2: 'http://gist.github.com/5546728'
  3: 'http://gist.github.com/5547019'
  5: 'http://gist.github.com/5547072'
compatibility:
  feature: outline
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`see individual properties`'
  'Applies to': 'All elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'see individual properties'
  Animatable: 'Yes'
  '[CSS Object Model Property](/css/concepts/cssom)': '`outline`'
  Percentages: N/A
readiness: 'Ready to Use'
summary: "The CSS outline property is a shorthand property for setting one or more of the individual outline properties outline-style, outline-width and outline-color in a single rule. In most cases the use of this shortcut is preferable and more convenient.\n"
tags:
  - CSS
  - Properties
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - css/properties/outline/af
    - css/properties/outline/ar
    - css/properties/outline/ast
    - css/properties/outline/az
    - css/properties/outline/bcc
    - css/properties/outline/bg
    - css/properties/outline/br
    - css/properties/outline/ca
    - css/properties/outline/cs
    - css/properties/outline/da
    - css/properties/outline/de
    - css/properties/outline/diq
    - css/properties/outline/el
    - css/properties/outline/eo
    - css/properties/outline/es
    - css/properties/outline/fa
    - css/properties/outline/fi
    - css/properties/outline/fr
    - css/properties/outline/gl
    - css/properties/outline/gu
    - css/properties/outline/he
    - css/properties/outline/hu
    - css/properties/outline/hy
    - css/properties/outline/id
    - css/properties/outline/it
    - css/properties/outline/ja
    - css/properties/outline/ka
    - css/properties/outline/kk
    - css/properties/outline/km
    - css/properties/outline/ko
    - css/properties/outline/ksh
    - css/properties/outline/kw
    - css/properties/outline/mk
    - css/properties/outline/ml
    - css/properties/outline/mr
    - css/properties/outline/ms
    - css/properties/outline/nl
    - css/properties/outline/no
    - css/properties/outline/oc
    - css/properties/outline/pl
    - css/properties/outline/pt
    - css/properties/outline/pt-br
    - css/properties/outline/ro
    - css/properties/outline/ru
    - css/properties/outline/si
    - css/properties/outline/sk
    - css/properties/outline/sl
    - css/properties/outline/sq
    - css/properties/outline/sr
    - css/properties/outline/ta
    - css/properties/outline/th
    - css/properties/outline/tr
    - css/properties/outline/uk
    - css/properties/outline/vi
    - css/properties/outline/yue
    - css/properties/outline/zh
    - css/properties/outline/zh-hans
    - css/properties/outline/zh-hant
    - css/properties/outline/zh-tw
translations:
  sv:
    text: svenska
    href: /css/properties/outline/sv
uri: css/properties/outline

---
## Summary

The CSS outline property is a shorthand property for setting one or more of the individual outline properties outline-style, outline-width and outline-color in a single rule. In most cases the use of this shortcut is preferable and more convenient.

Outlines differ from [borders](/css/properties/border) in the following ways:

-   Outlines do not take up space, they are drawn above the content.
-   Outlines may be non-rectangular. They are rectangular in Gecko/Firefox. Internet Explorer attempts to place the smallest contiguous outline around all elements or shapes that are indicated to have an outline. Opera draws a non-rectangular shape around a construct.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `see individual properties`

Applies to
:   All elements

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   see individual properties

Animatable
:   Yes

[CSS Object Model Property](/css/concepts/cssom)
:   `outline`

Percentages
:   N/A

## Syntax

-   `outline: inherit`
-   `outline: outline-color outline-style outline-width`

## Values

outline-color outline-style outline-width
:   The `outline` property can contain up to three components:

-   `outline-color`: This can take any valid CSS color as its value.
-   `outline-style`: This takes any of the range of style values available to the [**outline-style**](/css/properties/outline-style) property, which includes `none`, `dotted`, `dashed`, `solid`, `double`, `groove`, `ridge`, `inset`, `outset`. For more details about each, see the [**outline-style**](/css/properties/outline-style) page.
-   `outline-width`: This takes a numeric value with any of the standard length units.

inherit
:   This is a keyword indicating that the value is inherited from their parent's element calculated value.

## Examples

A simple example showing multiple **div**s, identical in style except that they have different **outline** properties applied to them.

``` html
<div class="one">I &hearts; WebPlatform.org!</div>
<div class="two">I &hearts; WebPlatform.org!</div>
<div class="three">I &hearts; WebPlatform.org!</div>
<div class="four">I &hearts; WebPlatform.org!</div>
<div class="five">I &hearts; WebPlatform.org!</div>
```

[View live example](http://code.webplatform.org/gist/5546931)

``` css
.one {
    /* The most basic border example you can show. */
    outline: 1px solid #000;
}

.two {
    /* If you don't explicitly set a color, currentColor is used, which
     equates to the text colour of the element, in this case black.   */
    outline: 4px dashed;
}

.three {
    /* When no width is specified, the default width medium is used */
    outline: dotted #f00;
}

.four {
    /* When no outline style is specified, the outline won't appear,
     as the default outline style is none. */
    outline: 5px #f00;
}

.five {
    /* A more interesting outline example to round things off. */
    outline: 10px inset #0f0;
}
```

[View live example](http://code.webplatform.org/gist/5546931)

Even though the syntax of outline and border is similar they differ in the way they are drawn.

``` css
/* Outlines do not take up space, they are drawn above the content */
.outline { outline: 10px solid #f00; }

/* Borders do */
.border { border: 10px solid #f00; }
```

[View live example](http://code.webplatform.org/gist/5546728)

An example of how outline and border behave when applied to an inline element spanning multiple lines.

``` html
<p>Web Platform Docs is a community-driven site that aims to become <span class="outline">a comprehensive and authoritative source for web developer documentation.</span></p>
<p>Web Platform Docs is a community-driven site that aims to become <span class="border">a comprehensive and authoritative source for web developer documentation.</span></p>
<p>Web Platform Docs is a community-driven site that aims to become <span class="outline border">a comprehensive and authoritative source for web developer documentation.</span></p>
```

[View live example](http://code.webplatform.org/gist/5547019)

``` css
/**
 * Outline vs Border on multiline text
 */

.outline {
    /* The outline is drawn all around the spanning element. */
    outline: 2px solid #f06;
}

.border {
    /* The border does not close at the edge of the element
     behaving as if it was a box. */
    border: 2px solid #00f;
}

/* The third paragraph has both outline and border */
```

[View live example](http://code.webplatform.org/gist/5547019)

Browsers place an outline around the element that currently has focus.

``` html
<p>Press the TAB key to navigate through the links below and focus them.</p>
<a href="http://webplatform.org">I &#9829; WebPlatform.org!</p>
<a class="two" href="http://webplatform.org">I &hearts; WebPlatform.org!</p>
```

[View live example](http://code.webplatform.org/gist/5547072)

``` css
/**
 * Outline, links and focus status
 */

/* Browsers place an outline around the element that currently has focus */

a {
    color: #f06;
    font: italic 200% Georgia, serif;
    text-decoration: none;
}

.two:focus {
    /* A different outline on focus for the second link */
    outline: 5px dotted #C67606;
}

a:active,
a:hover {
    /* Improve readability when focused
    and also mouse hovered in all browsers. */
    outline: 0;
}
```

[View live example](http://code.webplatform.org/gist/5547072)

## Notes

Displaying an outline does not cause reflow, no matter how wide the outline is. The outline frame is drawn over an element, and does not influence the position or size of the box, or of any other boxes.

## Related specifications

[CSS Basic User Interface Module Level 3 (CSS3 UI)](http://dev.w3.org/csswg/css-ui/#outline)
:   Working Draft
