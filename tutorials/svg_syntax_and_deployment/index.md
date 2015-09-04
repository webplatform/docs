---
title: svg syntax and deployment
tags:
  - Tutorials
  - SVG
readiness: 'In Progress'
notes:
  - 'Fix multiple broken links'
summary: 'This article shows the basic syntax and usage of SVG.'
uri: 'tutorials/svg syntax and deployment'
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - here
    - svgdemo1.png
    - 'Namespaces Crash Course'
    - 'this dedicated article'
    - 'on the next page'

---
# SVG syntax and deployment

## Summary

This article shows the basic syntax and usage of SVG.

## A Simple Example

Let us dive straight in with a simple example. Take a look at the following code.

    <svg version="1.1"
         baseProfile="full"
         xmlns="http://www.w3.org/2000/svg">

      <rect width="100%" height="100%" fill="red" />

      <circle cx="150" cy="100" r="80" fill="green" />

      <text x="150" y="125" font-size="60" text-anchor="middle" fill="white">SVG</text>

    </svg>

Copy the code and paste it in a file demo1.svg. Then open the file in Firefox. It will render as shown in the following screenshot. (Firefox users: click [here](/w/index.php?title=here&action=edit&redlink=1))

[svgdemo1.png](/w/index.php?title=svgdemo1.png&action=edit&redlink=1)

The rendering process involves the following:

1.  We start with the `svg` root element:
    -   a doctype declaration as known from (X)HTML should be left off because DTD based SVG validation lead to more problems than it solves
    -   to identify the version of the SVG for other types of validation the `version` and `baseProfile` attributes should always be used instead
    -   as an XML dialect, SVG must always bind the namespaces correctly (in the xmlns attribute). See the [Namespaces Crash Course](/w/index.php?title=Namespaces_Crash_Course&action=edit&redlink=1) page for more info.

2.  3.  The background is set to red by drawing a rectangle [[\<rect/\>]] that covers the complete image area
4.  A green circle [[\<circle/\>]] with a radius of 80px is drawn atop the center of the red rectangle (offset 30+120px inward, and 50+50px upward).
5.  The text "SVG" is drawn. The interior of each letter is filled in with white. The text is positioned by setting an anchor at where we want the midpoint to be: in this case, the midpoint should correspond to the center of the green circle. Fine adjustments can be made to the font size and vertical position to ensure the final result is aesthetically pleasing.

### Basic properties of SVG files

-   The first important thing to notice is the order of rendering of elements. The globally valid rule for SVG files is, that *later* elements are rendered *atop previous* elements. The further down an element is the more will be visible.
-   SVG files on the web can be displayed directly in the browser or embedded in HTML files via several methods:
    -   If the HTML is XHTML and is delivered as type `application/xhtml+xml`, the SVG can be directly embedded in the XML source.
    -   If the HTML is HTML5, and the browser is a conforming HTML5 browser, the SVG can be directly embedded, too. However, there may be syntax changes necessary to conform to the HTML5 specification
    -   The SVG file can be referenced with an `object` element:

                     <object data="image.svg" type="image/svg+xml" />

    -   Likewise an `iframe` element can be used:

                     <iframe src="image.svg"></iframe>

    -   An `img` element can be used theoretically, too. However this technique doesn't work in Firefox before 4.0.
    -   Finally SVG can be created dynamically with JavaScript and injected into the HTML DOM. This has the advantage, that replacement technologies for browsers, that can't process SVG, can be implemented.

-   See [this dedicated article](/w/index.php?title=this_dedicated_article&action=edit&redlink=1) for an in-depth dealing with the topic.
-   How SVG handles sizes and units will be explained [on the next page](/w/index.php?title=on_the_next_page&action=edit&redlink=1).

### SVG File Types

SVG files come in two flavors. Normal SVG files are simple text files containing SVG markup. The recommended filename extension for these files is ".svg" (all lowercase).

Due to the potentially massive size SVG files can reach when used for some applications (e.g., geographical applications), the SVG specification also allows for gzip-compressed SVG files. The recommended filename extension for these files is ".svgz" (all lowercase). Unfortunately it is very problematic to get gzip-compressed SVG files to work reliably across all SVG capable user agents when served from Microsofts IIS server, and Firefox can not load gzip-compressed SVG from the local computer. Avoid gzip-compressed SVG except when you are publishing to a webserver that you know will serve it correctly. For normal SVG files, servers should send the `Content-Type: image/svg+xml` HTTP header. For gzip-compressed SVG files, servers should also send the `Content-Encoding: gzip` header.

## Attribution

*This article contains content originally from external sources, including ones licensed under the CC-BY-SA license.* [![cc-by-sa-small-wpd.png](/assets/public/c/c8/cc-by-sa-small-wpd.png)](http://creativecommons.org/licenses/by-sa/3.0/us/)

Portions of this content copyright 2012 Mozilla Contributors. This article contains work licensed under the Creative Commons Attribution-Sharealike License v2.5 or later. The original work is available at Mozilla Developer Network: [Article](https://developer.mozilla.org/en-US/docs/SVG/Tutorial/Getting_Started)

