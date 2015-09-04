---
title: making css easier to read
tags:
  - Tutorials
  - CSS
readiness: 'Ready to Use'
summary: 'This article looks at the style and grammar of the CSS language itself, and how to make your CSS more readable using whitespace and comments.'
uri: 'tutorials/making css easier to read'

---
# Making CSS easier to read

## Summary

This article looks at the style and grammar of the CSS language itself, and how to make your CSS more readable using whitespace and comments.

## Information: Readable CSS

You can add whitespace and comments to your stylesheets to make them more readable. You can also group selectors together, when the same style rules apply to elements selected in different ways.

### White space

Whitespace means actual spaces, tabs and new lines. You can add white space to make your stylesheets more readable.

Your sample CSS files will currently have one rule per line, and almost the minimum of white space. In a complex stylesheet this layout would be difficult to read, making the stylesheet difficult to maintain.

The layout you choose is usually a personal preference, but if your stylesheets are part of shared projects, those projects might have their own conventions.

Some people like the compact layout that we have been using, only splitting a line when it becomes very long:

``` {.css}
.carrot {color: orange; text-decoration: underline; font-style: italic;}
```

 Some people prefer one property-value (selector, curly brace, etc.) per line:

``` {.css}
.carrot
{
color: orange;
text-decoration: underline;
font-style: italic;
}
```

 Some people prefer to put the first bracket on the same line as the selector:

``` {.css}
.carrot {
  color: orange;
  text-decoration: underline;
  font-style: italic;
}
```

 Some people use indention—two spaces, four spaces, or a tab are common:

``` {.css}
.carrot {
  color: orange;
  text-decoration: underline;
  font-style: italic;
}
```

 Some people like everything to line up vertically (but a layout like this is difficult to maintain):

``` {.css}
.carrot
{
  color:                 orange;
  text-decoration:       underline;
  font-style:            italic;
}
```

 Some people use tabs for the layout. Some people only use spaces.

### Comments

Comments in CSS begin with `/*` and end with `*/`. You can use comments to make actual comments in your stylesheet, and also to *comment out* parts of it temporarily for testing purposes. To comment out part of a stylesheet, place that part in a comment so that the browser ignores it. Be careful where you start and end the comment. The rest of the stylesheet must still have correct syntax.

``` {.css}
/* style for initial letter C in first paragraph */
.carrot {
  color: orange;
  text-decoration: underline;
  font-style: italic;
}
```

### Grouped selectors

When many elements have the same style, you can specify a group of selectors, separating them with commas. The declaration applies to all the selected elements.

Elsewhere in your stylesheet you can specify the same selectors again individually, to apply individual style rules to them.

This rule makes [h1], [h2], and [h3] elements the same color — it is convenient to specify the color in only one place, in case it has to be changed:

``` {.css}
/* color for headings */
h1, h2, h3 {color: navy;}
```

### Sorting properties

When used consistently sorting properties can be a great way to help make your stylesheets more readable. For instance sorting your properties by first properties that effects layout then color.

``` {.css}
/* sorted properties */
selector {
  width: 200px;
  height: 100px;
  background-color: yellow;
}
```

## Action: Adding comments and improving the layout

-   Edit your CSS file, and ensure that it has these rules in it (in any order):

``` {.css}
strong {color: red;}
.carrot {color: orange;}
.spinach {color: green;}
#first {font-style: italic;}
p {color: blue;}
```

<li>
Make it more readable by rearranging it in a way that you find logical, and by adding white space and comments in whatever way you think best.

</li>
<li>
Save the file and refresh your browser's display, to make sure that your changes do not affect how the stylesheet works.

</li>

## See also

### Exercise questions

Comment out part of your stylesheet, without changing anything else, to make the very first letter of your document red.

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/).

