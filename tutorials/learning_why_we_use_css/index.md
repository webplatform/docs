---
title: Why use CSS?
attributions:
  - 'This article contains content originally from external sources, including ones licensed under the CC-BY-SA license. [![cc-by-sa-small-wpd.png](/assets/public/c/c8/cc-by-sa-small-wpd.png)](http://creativecommons.org/licenses/by-sa/3.0/us/)'
  - 'Portions of this content copyright 2012 Mozilla Contributors. This article contains work licensed under the Creative Commons Attribution-Sharealike License v2.5 or later. The original work is available at Mozilla Developer Network: [Article](https://developer.mozilla.org/en-US/docs/CSS/Getting_Started/Why_use_CSS)'
readiness: 'Ready to Use'
summary: 'This tutorial looks at why we should use CSS, and why using CSS for styling our documents is better than using presentational HTML.'
tags:
  - Tutorials
  - CSS
uri: 'tutorials/learning why we use css'

---
## Summary

This tutorial looks at why we should use CSS, and why using CSS for styling our documents is better than using presentational HTML.

## Information: Why use CSS?

CSS helps you to keep the informational content of a document separate from the details of how to display it. The details of how to display the document are known as its *style*. You keep the style separate from the content so that you can:

-   Avoid duplication
-   Make maintenance easier
-   Use the same content with different styles for different purposes

Your web site might have thousands of pages that look similar. Using CSS, you store the style information in common files that all the pages share. When a user displays a web page, the user's browser loads the style information along with the content of the page. When a user prints a web page, you might provide different style information that makes the printed page easy to read.

In general, you use HTML to describe the content of the document, not its style; you use CSS to specify its style, not its content. There are exceptions to this rule, of course, and HTML also provides some ways to specify style. For example, in HTML you can use a `<b>` tag to make text bold, and you can specify the background colour of a page in its `<body>` tag. When you use CSS, you normally avoid using these HTML style features so that all your document's style information is in one place.

## Action: Creating a style sheet for an HTML document

### Creating the style sheet

1.  Create a text file; this file will be your style sheet. Name it `style1.css`

2.  In your CSS file, copy and paste this one line, then save the file:

    ``` css
    strong { color: red; }
    ```

### Linking your document to your stylesheet

1.  Create another text file; this file will be your HTML document. Name it whatever you like.

2.  In your HTML file, copy and paste the following lines; the `<link...>` line references your style sheet:

    ``` html
    <!DOCTYPE html>
     <html>
       <head>
       <meta charset="UTF-8">
       <title>Sample document</title>
       <link rel="stylesheet" href="style1.css">
       </head>
       <body>
         <p>
           <strong>C</strong>ascading
           <strong>S</strong>tyle
           <strong>S</strong>heets
         </p>
       </body>
     </html>
    ```

3.  Save the file and load it in a browser. The style sheet makes the letters inside the `<strong>` tags display in red, like this:

    **C**ascading **S**tyle **S**heets

## What next?

Now you have a sample document linked to a separate style sheet, you are ready to learn more about how your browser combines them when it displays the document. See the other tutorials in this section for more information.
