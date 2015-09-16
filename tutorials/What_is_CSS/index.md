---
title: 'What is CSS?'
attributions:
  - 'This article contains content originally from external sources, including ones licensed under the CC-BY-SA license. [![cc-by-sa-small-wpd.png](/assets/public/c/c8/cc-by-sa-small-wpd.png)](http://creativecommons.org/licenses/by-sa/3.0/us/)'
  - 'Portions of this content copyright 2012 Mozilla Contributors. This article contains work licensed under the Creative Commons Attribution-Sharealike License v2.5 or later. The original work is available at Mozilla Developer Network: [Article](https://developer.mozilla.org/en-US/docs/CSS/Getting_Started/What_is_CSS)'
readiness: 'Ready to Use'
summary: 'This tutorial answers the question &quot;what is CSS?&quot;.'
tags:
  - Tutorials
  - CSS
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - HTML
    - XML
    - XUL
uri: 'tutorials/What is CSS?'

---
## Summary

This tutorial answers the question &quot;what is CSS?&quot;.

## Information: What is CSS

Cascading Style Sheets (CSS) is a language for specifying how documents are presented to users.

A *document* is a collection of information that is structured using a *markup language*. Examples include:

-   A web page like the one you are reading is a document. The information that you see in a web page is usually structured using the markup language HTML (HyperText Markup Language).
-   Dialogs, also called modal windows, of an application are often documents. Such dialogs may also be structured using a markup language, like XUL. This is often the case in Mozilla applications, but is not the common case.

In this tutorial, boxes captioned **More details** like the one below contain optional information. If you are in a hurry to progress with the tutorial then you could skip these boxes, perhaps returning to read them later. Otherwise read them when you come to them, and perhaps follow the links to learn more.

### More details

A document is not the same as a file. It might or might not be stored in a file.

For example, the document that you are reading now is not stored in a file. When your web browser requests this page, the server queries a database and generates the document, gathering parts of the document from many files. However, in this tutorial you will work with documents that are stored in files.

For more information about documents and markup languages, see other parts of this web site—for example:

||
|[HTML](/w/index.php?title=HTML&action=edit&redlink=1)|for web pages|
|[XML](/w/index.php?title=XML&action=edit&redlink=1)|for structured documents in general|
|[SVG](/svg)|for graphics|
|[XUL](/w/index.php?title=XUL&action=edit&redlink=1)|for user interfaces in Mozilla|

In Part II of this tutorial you will see examples of these markup languages.

*Presenting* a document to a user means converting it into a form that humans can make use of. Browsers, like Firefox, Chrome or Internet Explorer, are designed to present documents visually — for example, on a computer screen, projector or printer.

CSS is not just for browsers, and not just for visual presentation. In formal CSS terminology, the program that presents a document to a user is called a *user agent* (UA). A browser is just one kind of UA. However, in Part I of this tutorial you will only work with CSS in a browser.

For some formal definitions of terminology relating to CSS, see the [CSS Specification](http://www.w3.org/TR/CSS2/).

## Action: Creating a document

1.  Use your computer to create a new directory and a new text file there. The file will contain your document.

2.  Copy and paste the HTML shown below. Save the file using the name `doc1.html`

        <!DOCTYPE html>
         <html>
           <head>
           <meta charset="UTF-8">
           <title>Sample document</title>
           </head>

           <body>
             <p>
               <strong>C</strong>ascading
               <strong>S</strong>tyle
               <strong>S</strong>heets
             </p>
           </body>
         </html>

3.  In your browser, open a new tab or a new window, and open the file there. You should see the text with the initial letters bold, like this:

    **C**ascading **S**tyle **S**heets

    What you see in your browser might not look exactly the same as this, because of settings in your browser and in this wiki. If there are some differences in the font, spacing and colors that you see, they are not important.

## What next?

Your document does not yet use CSS. In the next article you will use CSS to specify its style.
