---
title: 'CSS text quick start'
attributions:
  - 'This article contains content originally from external sources, including ones licensed under the CC-BY-SA license. [![cc-by-sa-small-wpd.png](/assets/public/c/c8/cc-by-sa-small-wpd.png)](http://creativecommons.org/licenses/by-sa/3.0/us/)'
  - 'Portions of this content copyright 2012 Mozilla Contributors. This article contains work licensed under the Creative Commons Attribution-Sharealike License v2.5 or later. The original work is available at Mozilla Developer Network: [Article](https://developer.mozilla.org/en-US/docs/CSS/Getting_Started/Text_styles)'
readiness: 'Ready to Use'
summary: 'This tutorial provides a quick instruction on styling text with CSS.'
tags:
  - Tutorials
  - CSS
uri: 'tutorials/css text quick start'

---
## Summary

This tutorial provides a quick instruction on styling text with CSS.

## Information on text styles

CSS has several properties for styling text.

There is a convenient shorthand property, **font**, which you can use to specify several aspects at once—for example:

-   Bold, italic, and small-caps (small capital letters)
-   The size
-   The line height
-   The font typeface

Consider this example:

``` css
p {font: italic 75%/125% "Comic Sans MS", cursive;}
```

This rule sets various font properties, making all paragraphs italic.

-   The font size is set to three-quarters of the size in each paragraph's parent element, and the line height is set to 125% (spaced a little wider than normal).
-   The font typeface is set to Comic Sans MS, but if this typeface is not available, then the browser will use its default cursive (hand-written) typeface.

The rule has the side-effect of turning off of bold and small-caps (setting them to `normal`):

### Font faces

You cannot predict what typefaces visitors of your site will have. So when you specify font typefaces, it is a good idea to give a list of alternatives in order of preference. End the list with one of the built-in default typefaces: `serif`, `sans-serif`, `cursive`, `fantasy` or `monospace`.

If the typeface does not support some features in the document, then the browser can substitute a different typeface. For example, the document might contain special characters that the typeface does not support. If the browser can find another typeface that has those characters, then it will use the other typeface.

To specify a typeface on its own, use the [font-family] property.

### Font sizes

Browser users can override the default font sizes or change the text size while they read a page, so it makes good sense for you to use relative sizes wherever you can.

You can use some built-in values for font sizes, like `small`, `medium` and `large`. You can also use values relative to the font size of the parent element, like: `smaller`, `larger`, `150%` or `1.5em`. An "em" is equivalent to the width of the letter "m" (for the font size of the parent element); thus 1.5em is one-and-a-half times the size of the font of the parent element.

If necessary, you can specify an actual size, like this: `14px` (14 pixels) for a display device or 14pt (14 points) for a printer. This practice does not promote accessibility for visually impaired users, because it does not allow them to change the size of text characters. A more accessible strategy is to set a built-in value like medium on a top-level element of the document, and then set relative sizes for all its descendent elements.

To specify a font size on its own, use the [font-size] property.

### Line height

The line height property specifies the spacing between lines. If your document has long paragraphs that contain many lines, a larger-than-normal spacing value makes text easier to read, especially if the font size is small.

To specify a line height on its own, use the [line-height] property.

### Decoration

The separate [text-decoration] property can specify other styles, like `underline` or `line-through`. You can set it to `none` to explicitly remove any decoration.

### Other properties

To specify italic on its own, use `[font-style]: italic;`
 To specify bold on its own, use `[font-weight]: bold;`
 To specify small capitalized letters on its own, use `[font-variant]: small-caps;`

To turn any of these off individually, you can specify the value `normal` or `inherit`.

## More details on applying text styles

You can specify text styles in a variety of other ways. For example, some of the properties mentioned here have other values that you can use. In a complex style sheet, avoid using the shorthand `font` property, because of its side-effects (resetting other individual properties).

For full details of the properties that relate to fonts, see [Fonts](http://www.w3.org/TR/CSS21/fonts.html) in the CSS Specification. For full details of text decoration, see [Text](http://www.w3.org/TR/css3-text/) there. If you do not want to depend on the typefaces installed on visitors' systems, you can use [@font-face](/css/atrules/@font-face) to specify an online font. However, this requires that the visitors are using a browser that supports this rule.

## Action: Specifying fonts

For a simple document, you can set the font of the `<body>` element and the rest of the document inherits the settings.

1.  Edit your CSS file.

2.  Add the following rule to change the font throughout the document. The top of the CSS file is a logical place for it, but it has the same effect wherever you put it:

    ``` css
    body {font: 16px "Comic Sans MS", cursive;}
    ```

3.  Add a comment explaining the rule, and add white space to make it match your preferred layout.

4.  Save the file and refresh your browser to see the effect. If your system has Comic Sans MS, or another cursive font that does not support italic, then your browser chooses a different font face for the italic text in the first line.

5.  From your browser's menu bar, choose **View \> Text Size \> Increase** (or **View \> Zoom \> Zoom In**). Even though you specified 16 pixels in the CSS style, a visitor reading the page can change the size of the text.

## Conclusion

This article provides a quick introduction to styling text with CSS. For more in-depth information, see the other tutorial articles in this series.

## See also

### Exercise questions

Without changing anything else, make all six initial letters twice the size in the browser's default serif font.
