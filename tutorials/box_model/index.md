---
title: 'Exploring the CSS box model'
attributions:
  - 'This article contains content originally from external sources, including ones licensed under the CC-BY-SA license. [![cc-by-sa-small-wpd.png](/assets/public/c/c8/cc-by-sa-small-wpd.png)](http://creativecommons.org/licenses/by-sa/3.0/us/)'
  - 'Portions of this content copyright 2012 Mozilla Contributors. This article contains work licensed under the Creative Commons Attribution-Sharealike License v2.5 or later. The original work is available at Mozilla Developer Network: [Article](https://developer.mozilla.org/en-US/docs/CSS/Getting_Started/Boxes)'
code_samples:
  - 'http://code.webplatform.org/gist/11409432'
  - 'http://code.webplatform.org/gist/11411135'
  - 'http://code.webplatform.org/gist/11429299'
  - 'http://code.webplatform.org/gist/11429444'
  - 'http://code.webplatform.org/gist/11429785'
  - 'http://code.webplatform.org/gist/11431094'
readiness: 'Ready to Use'
summary: 'This article briefly describes the CSS box model and how the elements are laid out when they are displayed in the browser.'
tags:
  - Tutorials
  - CSS
uri: 'tutorials/box model'

---
## Summary

This article briefly describes the CSS box model and how the elements are laid out when they are displayed in the browser.

## Information: Box Model

When your browser displays an element, the element takes up space. You can think of all HTML elements as boxes. All boxes have certain dimensions and are specified by four properties: a content area of the element (e.g., a picture, a text header, etc.) and the optional [padding](/css/properties/padding), [border](/css/properties/border) and [margin](/css/properties/margin) properties.

The element is in the center and displays its content. Around that, there is padding. Around that, there is a border. Around that, there is a margin that separates the element from other elements.

The "edges" or the perimeters of each of the previous areas can have different properties defined on them.

Thus the content edge can have a certain width or height, the padding edge that surrounds the content can have a certain width or height, etc. Any or all of these sizes can be zero.

Each property that surrounds the content can be broken down into a top, right, bottom, or a left part for example margin-left, padding-bottom, border-left, etc.

In this [Live Example](http://code.webplatform.org/gist/11409432) we see a typical declaration of a div element that we specify a width, a margin and a padding.

### Coloring

You can specify a color for the element backround and the padding will also get the same one automatically. The border can have its own color but the margin is always transparent so you cannot color it.

|Property|Color|
|:-------|:----|
|Margin|Always transparent|
|Element|Same as background color (if any)|
|Padding|Gets elements background color|
|Border|Same as border-color property (if any)|

### Borders

You can use borders to decorate elements with lines or boxes. To specify the same border all around an element, use the [border](/css/properties/border) property. Specify the width (usually in pixels for display on a screen), the style, and the color.

The styles are:

 none
:   no border
 dotted
:   border as a series of dots
 dashed
:   border as a series of dashes
 solid
:   border as single lines
 double
:   border as two single lines with the same width as the [border-width](/css/properties/border-width) property
 groove
:   border as a grooved etched line
 ridge
:   border as a ridged etched line
 inset
:   border looks like its coming inside the element
 outset
:   opposite of inset. Border looks like its coming out of the element

See the [Live Example](http://code.webplatform.org/gist/11411135) of border styles

You can also set the style to `hidden` which is the same as none to explicitly remove the border, or set the color to `transparent` to make the border invisible without changing the layout.

To specify borders one side at a time, use the properties: [border-top](/css/properties/border-top) , [border-right](/css/properties/border-right) , [border-bottom](/css/properties/border-bottom) , [border-left](/css/properties/border-left) . You can use these to specify a border on only one side, or different borders on different sides.

#### Border sides example

This rule sets the dimensions, the background color and the top border of all div elements:

``` css
 div {
        width: 200px;
    height: 100px;   /* required to give divs some height */
    border-top: 4px solid green;
        background-color: yellow;
        color: dark-green;
}
```

 The result looks like this [Live Example](http://code.webplatform.org/gist/11429299).

This rule makes images easier to see by giving them a mid-gray border all round:

``` css
img {border: 2px solid #ccc;}
```

 The result looks like this [Live Example](http://code.webplatform.org/gist/11429444).

### Margins and padding

You use margins and padding to adjust elements' positions and to create space around them. Use the [margin](/css/properties/margin) property or the [padding](/css/properties/padding) property to set the margin or padding widths respectively.

If you specify one width, it applies all around the element (top, right, bottom and left). If you specify two widths, the first applies to the top and bottom, the second to the right and left. You can specify all four widths in the order: top, right, bottom, left.

### Margin and padding example

This rule marks out paragraphs with the class `remark` by giving them a red border all round. Padding all round separates the border from the text a little. A left margin indents the paragraph relative to the rest of the text:

``` css
p.remark {
  border: 2px solid red;
  padding: 4px;
  margin-left: 24px;
}
```

 The result looks like this [Live Example](http://code.webplatform.org/gist/11429785).

## More details

When you use margins and padding to adjust the way elements are laid out, your style rules interact with the browser's defaults in ways that can be complex. Different browsers lay elements out differently. The results might look similar until your stylesheet changes things. Sometimes this can make your stylesheet give surprising results.

To get the result you want, you might have to change your document's markup. Other tutorials in this series have more information on this.

## Action: Adding borders

-   Edit your CSS file, `style2.css`. Add this rule to draw a line across the page over each heading:

``` css
h3 {border-top: 1px solid gray;}
```

-   If you took the challenge on the last page, modify the rule you created, otherwise add this new rule to add space underneath each list item:

``` css
li {
  list-style: lower-roman;
  margin-bottom: 8px;
}
```

-   Refresh your browser to see the [Result](http://code.webplatform.org/gist/11431094).

## See also

### Exercise questions

1.  Add one rule to your stylesheet, making a wide border all around the oceans in a color that reminds you of the sea.
2.  Look at a random website and see if you can find a paragraph or a section and guess that box model. Write down in a piece of paper their padding, margin, border properties. Then compare them to the actual CSS layout as you inspect the element in your browser.
