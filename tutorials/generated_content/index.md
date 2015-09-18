---
title: 'Generating content with CSS'
attributions:
  - 'This article contains content originally from external sources, including ones licensed under the CC-BY-SA license. [![cc-by-sa-small-wpd.png](/assets/public/c/c8/cc-by-sa-small-wpd.png)](http://creativecommons.org/licenses/by-sa/3.0/us/)'
  - 'Portions of this content copyright 2012 Mozilla Contributors. This article contains work licensed under the Creative Commons Attribution-Sharealike License v2.5 or later. The original work is available at Mozilla Developer Network: [Article](https://developer.mozilla.org/en-US/docs/CSS/Getting_Started/Content)'
readiness: 'Ready to Use'
summary: 'This article describes generated content — a way in which you can use CSS to add content when a document is displayed.'
tags:
  - Tutorials
  - CSS
uri: 'tutorials/generated content'

---
## Summary

This article describes generated content — a way in which you can use CSS to add content when a document is displayed.

## Information: Content

One of the important advantages of CSS is that it helps you to separate a document's style from its content. Yet there are situations where it makes sense to specify certain content as part of the stylesheet, not as part of the document. Content specified in a stylesheet can consist of text or images. You specify content in your stylesheet when the content is closely linked to the document's structure.

## Generated content in detail

Specifying content in a stylesheet can cause complications. For example, you might have different language versions of your document that share a stylesheet. If part of the stylesheet has to be translated, it means that you must put those parts of the stylesheet in separate files and arrange for them to be linked with the appropriate language versions of your document.

These complications do not arise if the content you specify consists of symbols or images that apply in all languages and cultures.

Content specified in a stylesheet does not become part of the DOM.

### Text content

CSS can insert text content before or after an element. To specify this, make a rule and add [::before](/css/selectors/pseudo-elements/::before) or [::after](/css/selectors/pseudo-elements/::after) to the selector. In the declaration, specify the [content](/css/properties/content) property with the text content as its value.

#### Generated text example

This rule adds the text Reference: before every element with the class `ref`:

``` css
.ref:before {
  font-weight: bold;
  color: navy;
  content: "Reference: ";
}
```

#### More details

The character set of a stylesheet is UTF-8 by default, but it can be specified in the link, or in the stylesheet itself, or in other ways. For details, see [4.4 CSS style sheet representation](http://www.w3.org/TR/CSS21/syndata.html#q23) in the CSS Specification.

Individual characters can also be specified by an escape mechanism that uses backslash as the escape character. For example, \\265B is the chess symbol for a black queen. For details, see [Referring to characters not represented in a character encoding](http://www.w3.org/TR/CSS21/syndata.html#q24) and also [Characters and case](http://www.w3.org/TR/CSS21/syndata.html#q6) in the CSS Specification.

### Generated images

To add an image before or after an element, you can specify the URL of an image file in the value of the **content** property.

#### Generated image example

This rule adds a space and an icon after every link that has the class `glossary`:

``` css
a.glossary:after {content: " " url("../images/glossary-icon.gif");}
```

 To add an image as an element's background, specify the URL of an image file in the value of the [background](/css/properties/background) property. This is a shorthand property that specifies the background color, the image, how the image repeats, and some other details.

The following element rule sets the background of a specific element, using a URL to specify an image file. The selector specifies the element's id. The value `no-repeat` makes the image appear only once:

``` css
#sidebar-box {background: url("../images/sidebar-ground.png") no-repeat;}
```

#### More details

For information about individual properties affecting backgrounds, and about other options when you specify background images, see the **background** reference page.

## Action: Adding a background image

This image is a white square with a blue line at the bottom:

![Blue-rule.png](//static.webplatform.org/d/d3/Blue-rule.png)

1.  Download the image file into the same directory as your CSS file. (For example, right-click it to get a context menu, then choose Save Image As and specify the directory that you are using for this tutorial.)

2.  Edit your CSS file and add this rule to the body, setting a background image for the entire page.

    ``` css
    background: url("Blue-rule.png");
    ```

The value `repeat` is the default, so it does not need to be specified. The image repeats horizontally and vertically, giving an appearance like lined writing paper:

![Blue-rule-ground.png](//static.webplatform.org/9/93/Blue-rule-ground.png)

## See also

### Exercise question

1.  Download this image:

    ![Yellow-pin.png](//static.webplatform.org/9/98/Yellow-pin.png)

2.  Add a one rule to your stylesheet so that it displays the image at the start of each line:

    ![Blue-rule-ground-2.png](//static.webplatform.org/a/a2/Blue-rule-ground-2.png)

