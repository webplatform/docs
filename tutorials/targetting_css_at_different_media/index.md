---
title: Targeting CSS at different media types
attributions:
  - 'This article contains content originally from external sources, including ones licensed under the CC-BY-SA license. [![cc-by-sa-small-wpd.png](/assets/public/c/c8/cc-by-sa-small-wpd.png)](http://creativecommons.org/licenses/by-sa/3.0/us/)'
  - 'Portions of this content copyright 2012 Mozilla Contributors. This article contains work licensed under the Creative Commons Attribution-Sharealike License v2.5 or later. The original work is available at Mozilla Developer Network: [Article](https://developer.mozilla.org/en-US/docs/CSS/Getting_Started/Media)'
readiness: 'Ready to Use'
summary: 'This article focuses on using media types to target CSS at different type of media — screen, print, etc.'
tags:
  - Tutorials
uri: 'tutorials/targetting css at different media'

---
## <span>Summary</span>

This article focuses on using media types to target CSS at different type of media — screen, print, etc.

Many of the articles in this tutorial group have focused on the CSS properties and values that you can use to specify how to display a document. This page looks again at the purpose and structure of CSS stylesheets.

## <span>Information: Media</span>

The purpose of CSS is to specify how documents are presented to the user. Presentation can take more than one form.

For example, you are probably reading this page on a display device. But you might also want to project it on a screen for a large audience, or print it. These different media can have different characteristics. CSS provides ways to present a document differently in different media.

To specify rules that are specific to a type of media, use **@media**, followed by the media type, followed by curly braces that enclose the rules.

#### <span>Example</span>

A document on a web site has a navigation area to allow the user to move around the site.

In the markup language, the navigation area's parent element has the **id** `nav-area`. (In HTML5, this can be marked up with the `nav` element instead of a `div` with an **id** attribute.)

When the document is printed the navigation area has no purpose, so the stylesheet removes it completely:

    @media print {
      #nav-area {display: none;}
      }

Some of the common media types are:

||
|`screen`|Color computer display|
|`print`|Paged media|
|`projection`|Projected display|
|`all`|All media (the default)|

#### <span>More details</span>

There are other ways to specify the media type of a set of rules.

 The document's markup language might allow the media type to be specified when the stylesheet is linked to the document. For example, in HTML you can optionally specify the media type with a `media` attribute in the `LINK` tag.

 In CSS you can use `@import` at the start of a stylesheet to import another stylesheet from a URL, optionally specifying the media type.

 By using these techniques you can separate style rules for different media types into different files. This is sometimes a useful way to structure your stylesheets.

 For full details of media types, see [Media Queries](http://www.w3.org/TR/css3-mediaqueries/) in the CSS Specification.

 There are more examples of the `display` property in a later page in this tutorial, [Styling XML with CSS](/tutorials/styling_xml_with_css).

### <span>Printing</span>

CSS has some specific support for printing and for paged media in general.

 A `@page` rule can set the page margins. For double-sided printing, you can specify the margins separately for `@page:left` and `@page:right`.

 For print media, you normally use appropriate length units like inches (`in`) and points (`pt` = 1/72 inch), or centimeters (`cm`) and millimeters (`mm`). It is equally appropriate to use ems (`em`) to match the font size, and percentages (`%`).

 You can control how the content of the document breaks across page boundaries, by using the `page-break-before`, `page-break-after` and `page-break-inside` properties.

#### <span>Example</span>

This rule sets the page margins to one inch on all four sides:

    @page {margin: 1in;}

This rule ensures that every H1 element starts on a new page:

    h1 {page-break-before: always;}

#### <span>More details</span>

For full details of CSS support for paged media, see [Paged Media](http://www.w3.org/TR/css3-page/) in the CSS Specification.

 Like other features of CSS, printing depends on your browser and its settings. For example, your Mozilla browser supplies default margins, headers and footers when it prints. When other users print your document, you probably cannot predict the browser and the settings that they will use, so you probably cannot control the results completely.

### <span>User interfaces</span>

CSS has some special properties for devices that support a user interface, like computer displays. These make the document's appearance change dynamically as the user works with the interface.

 There is no special media type for devices with user interfaces.

 There are five special selectors:

||
|**Selector**|**Selects**|
|`E:hover`|Any E element that has the pointer over it|
|`E:focus`|Any E element that has keyboard focus|
|`E:active`|The E element that is involved in the current user action|
|`E:link`|Any E element that is a hyperlink to a URL that the user has *not* visited recently|
|`E:visited`|Any E element that is a hyperlink to a URL that the user *has* visited recently|

**Note:**The information that can be obtained from the :visited selector is restricted in `gecko 2.0`. See [Privacy and the :visited selector](https://developer.mozilla.org/en-US/docs/Web/CSS/Privacy_and_the_:visited_selector) for more details.

 The `cursor` property specifies the shape of the pointer: Some of the common shapes are:

||
|**Selector**|**Selects**|
|`pointer`|Indicating a link|
|`wait`|Indicating that the program cannot accept input|
|`progress`|Indicating that the program is working, but can still accept input|
|`default`|The default (usually an arrow)|

An `outline` property creates an outline that is often used to indicate keyboard focus. Its values are similar to the `border` property, except that you cannot specify individual sides.

 Some other features of user interfaces are implemented using attributes, in the normal way. For example, an element that is disabled or read-only has the **disabled** attribute or the **readonly** attribute. Selectors can specify these attributes like any other attributes, by using square brackets.

#### <span>Example</span>

These rules specify styles for a button that changes dynamically as the user interacts with it:

    .green-button {
      background-color:#cec;
      color:#black;
      border:2px outset #cec;
      }

    .green-button[disabled] {
      background-color:#cdc;
      color:#777;
      }

    .green-button:active {
      border-style: inset;
      }

This wiki does not support a user interface on the page, so these buttons do not "click". Here are some static images to illustrate the idea:

<table border="1">
<tr>
<td>
<table border="1">
<tr>
<td>
Click Me

</td>
<td>
Click Me

</td>
<td>
Click Me

</td>
</tr>
<tr>
<td>
</td>
</tr>
<tr>
<td>
disabled

</td>
<td>
normal

</td>
<td>
active

</td>
</tr>
</table>
</td>
</tr>
</table>
A fully functional button also has a dark outline around the entire button when it is the default, and a dotted outline on the face of the button when it has keyboard focus. It might also have a hover effect when the pointer is over it.

#### <span>More details</span>

For more information about user interfaces in CSS, see [User interface](http://www.w3.org/TR/css3-ui/) in the CSS Specification.

## <span>Action: Printing a document</span>

1. Make a new HTML document, `doc4.html`. Copy and paste the content from here:

     <!DOCTYPE html>
     <html>
       <head>
         <title>Print sample</title>
         <link rel="stylesheet" href="style4.css">
       </head>
       <body>
         <h1>Section A</h11>
         <p>This is the first section...</p>
         <h1>Section B</h1>
         <p>This is the second section...</p>
         <div id="print-head">
           Heading for paged media
         </div>
         <div id="print-foot">
           Page:     </div>
     </body>
     </html>

2. Make a new stylesheet, `style4.css`. Copy and paste the content from here:

     /*** Print sample ***/
      /* defaults  for screen */
     #print-head, #print-foot {   display: none;   }
      /* print only */
     @media print {
      h1 {   page-break-before: always;   padding-top: 2em;   }
      h1:first-child {   page-break-before: avoid;   counter-reset: page;   }
      #print-head {   display: block;   position: fixed;   top: 0pt;   left:0pt;   right: 0pt;    font-size: 200%;   text-align: center;   }
      #print-foot {   display: block;   position: fixed;   bottom: 0pt;   right: 0pt;    font-size: 200%;   }
      #print-foot:after {   content: counter(page);   counter-increment: page;   }
      }
     /* end print only */

3. View this document in your browser; it uses your browser's default style.

4. Print (or print preview) the document; the stylesheet places each section on a separate page, and it adds a header and footer to each page. If your browser supports counters, it adds a page number in the footer.

### <span>Challenges</span>

-   Move the print-specific style rules to a separate CSS file.
-   Read the `@import` reference page to find details of how to import the new print-specific CSS file into your `style4.css` stylesheet.
-   Make the headings turn blue when the mouse pointer is over them.

## <span>What next?</span>

So far, all the style rules in this tutorial have been specified in files. The rules and their values are fixed. The next page describes how you can change rules dynamically by using a programming language called **[JavaScript](/javascript)**.

