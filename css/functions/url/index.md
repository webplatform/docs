---
title: CSS images: url()
notes:
  - 'Include examples, specifications, compatibility.'
readiness: 'In Progress'
summary: 'CSS has a variety of different properties that can reference an image file, displaying that file on a web page normally as part of an element''s background. This is done using the CSS image syntax, which is url().'
tags:
  - CSS
  - Functions
uri: css/functions/url()

---
## <span>Summary</span>

CSS has a variety of different properties that can reference an image file, displaying that file on a web page normally as part of an element's background. This is done using the CSS image syntax, which is url().

## <span>Usage</span>

Usage is simple — you insert the path to the image you want to include in your page inside the brackets of `url()`, for example:

    background-image: url('images/my-image.png');

Note about formatting: The quotes around the URL can be either single or double quotes, and they are optional. However, if you are including some special characters such as single or double quotes, parentheses, and white space, then if the URL is not quoted, those special characters need to be escaped with a backslash(\\).

This will cause `my-image.png` to be displayed in the background of whatever element or elements the `background-image` property is applied to. Accepted image formats are:

-   .bmp
-   .gif
-   .png
-   .svg (this includes references to in-page SVG elements, for example `url(#mySVGElement)`)
-   data URIs
-   .webp

## <span>Browser support notes</span>

-   IE \< 9: doesn't support SVG for background-images, or multiple background images, or gradients
-   IE6: doesn't support PNG transparency properly; result looks buggy and malformed
-   Only Opera and Chrome support .webp

## <span>Properties that accept URL as a value</span>

-   [background-image](/css/properties/background-image)
-   [border-image](/css/properties/border-image)
-   [content](/css/properties/content)
-   [list-style-image](/css/properties/list-style-image)

**Needs Examples**: This section should include examples.

