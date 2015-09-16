---
title: 'writing-mode'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/5833192'
  - 'http://gist.github.com/5860978'
compatibility:
  feature: writing-mode
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`horizontal-tb`'
  'Applies to': 'All elements except table row groups, table column groups, table rows, and table columns'
  '[Inherited](/css/concepts/inherited)': 'Yes'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'specified value'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`writingMode`'
  Percentages: N/A
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'writing-mode specifies if lines of text are laid out horizontally or vertically, and the direction which lines of text and blocks progress.'
tags:
  - CSS
  - Properties
uri: css/properties/writing-mode

---
## Summary

writing-mode specifies if lines of text are laid out horizontally or vertically, and the direction which lines of text and blocks progress.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `horizontal-tb`

Applies to
:   All elements except table row groups, table column groups, table rows, and table columns

[Inherited](/css/concepts/inherited)
:   Yes

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   specified value

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:   `writingMode`

Percentages
:   N/A

## Syntax

-   `writing-mode: horizontal-tb`
-   `writing-mode: vertical-lr`
-   `writing-mode: vertical-rl`

## Values

horizontal-tb
:   Lines of text are laid out horizontally, and progress from the top to the bottom of the page. This is the writing mode used in many writing systems, such as Latin, Greek, Cyrillic, Arabic, Hebrew, etc.

vertical-rl
:   Lines of text are laid out vertically, and progress from the right to the left of the page. Asian languages, such as Chinese or Japanese traditionally used this writing mode.

vertical-lr
:   Lines of text are laid out vertically, and progress from the left to the right of the page. Mongolian-based writing systems typically use this writing mode.

## Examples

Sets the writing mode to vertical and to progress from right to left. Sometimes used by East Asian, especially Japanese and Chinese. This example is Japanese use case.

``` html
<p>日本では、新聞や書籍などで縦書きを使用することがあります。これは、縦書きのシンプルな例です。</p>
```

[View live example](http://code.webplatform.org/gist/5833192)

``` css
p {
    width: 100%;
    -webkit-writing-mode: vertical-rl;
}
```

Sets the writing mode, including a fallback for the previous version of the spec, supported by IE.

``` css
/* horizontal and top to bottom */
writing-mode: horizontal-tb;
-ms-writing-mode: lr-tb;

/* horizontal and top to bottom, and the direction of text to right to left */
writing-mode: horizontal-tb;
-ms-writing-mode: rl-tb;
direction: rtl;

/* vertical and to progress from right to left */
writing-mode: vertical-rl;
-ms-writing-mode: tb-rl;

/* vertical and to progress from left to right */
writing-mode: vertical-lr;
-ms-writing-mode: tb-lr;
```

Complete example, including HTML.

``` html
<style>
    #horizontal-tb {
    -ms-writing-mode: lr-tb;  /* old syntax, supported by IE */
    writing-mode: horizontal-tb;  /* modern syntax. WebKit currently requires prefix */
    }
   #horizontal-tb-direction-rtl {
    -ms-writing-mode: rl-tb;
        writing-mode: horizontal-tb;

        direction: rtl; /* sets the direction of text in a line to right to left */
   }
   #vertical-rl {
        -ms-writing-mode: tb-rl;
    writing-mode: vertical-rl;
    }
    #vertical-lr {
    -ms-writing-mode: tb-lr;
        writing-mode: vertical-lr;
    }
</style>
<div id="horizontal-tb">
    <h1>Writing-mode: horizontal-tb/lr-tb</h1>
    <p>This text should be horizontal, left to right, and <em>under</em> the heading.</p>
    <ol>
        <li>One</li>
    <li>Two</li>
    <li>Three</li>
    </ol>
</div>
<div id="horizontal-tb-direction-rtl">
    <h1>Writing-mode: horizontal-tb/rl-tb, direction: rtl</h1>
    <p>This text should be horizontal, right to left, and <em>under</em> the heading.</p>
    <ol>
    <li>One</li>
    <li>Two</li>
    <li>Three</li>
    </ol>
</div>
<div id="vertical-rl">
        <h1>Writing-mode: vertical-rl/tb-rl</h1>
        <p>This text should be vertical, and to the <em>left</em> of the heading.</p>
     <ol>
              <li>One</li>
              <li>Two</li>
          <li>Three</li>
     </ol>
</div>
<div id="vertical-lr">
    <h1>Writing-mode: vertical-lr/tb-lr</h1>
    <p>This text should be vertical, and to the <em>right</em> of the heading.</p>
    <ol>
        <li>One</li>
        <li>Two</li>
        <li>Three</li>
    </ol>
</div>
```

[View live example](http://code.webplatform.org/gist/5860978)

## Related specifications

[CSS Writing Modes Module Level 3](http://www.w3.org/TR/css3-writing-modes/#writing-mode)
:   W3C Working Draft

## See also

### Other articles

-   [direction](/css/properties/direction)
-   [unicode-bidi](/css/properties/unicode-bidi)

### External resources

-   [Vertical text with CSS 3 Writing Modes](http://generatedcontent.org/post/45384206019/writing-modes)
