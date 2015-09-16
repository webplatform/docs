---
title: about javascript
tags:
  - JavaScript
uri: 'concepts/programming/about javascript'

---
JavaScript is a cross-platform, object-based scripting language. This guide explains everything you need to know about using JavaScript.

## New features in JavaScript versions

``` js
/* Note: To add a link to new JavaScript version description
add version number to versionList variable below. The page linked to
must reside in /en/JavaScript/New_in_JavaScript/N, where N is version number. */

var versionList = ["1.5", "1.6", "1.7", "1.8", "1.8.1", "1.8.5"];
var s = "";
<ul>
  foreach (var i in versionList){
    let s = "/en/JavaScript/New_in_JavaScript/" .. i;
    <li>web.link(s, wiki.getPage(s).title)</li>;
  }
</ul>;
```

## What you should already know

This guide assumes you have the following basic background:

-   A general understanding of the Internet and the World Wide Web (WWW).
-   Good working knowledge of HyperText Markup Language (\<a href="mks://localhost/en/HTML" title="en/HTML"\>HTML\</a\>).

Some programming experience with a language such as C or Visual Basic is useful, but not required.

## JavaScript versions

<table class="standard-table">
<caption style="text-align: left;">
Table 1 JavaScript and Navigator versions

</caption>
\<thead\>

<tr>
<th scope="col">
JavaScript version

</th>
<th scope="col">
Navigator version

</th>
</tr>
\</thead\> \<tbody\>

<tr>
<td>
JavaScript 1.0

</td>
<td>
Navigator 2.0

</td>
</tr>
<tr>
<td>
JavaScript 1.1

</td>
<td>
Navigator 3.0

</td>
</tr>
<tr>
<td>
JavaScript 1.2

</td>
<td>
Navigator 4.0-4.05

</td>
</tr>
<tr>
<td>
JavaScript 1.3

</td>
<td>
Navigator 4.06-4.7x

</td>
</tr>
<tr>
<td>
JavaScript 1.4

</td>
<td>
</td>
</tr>
<tr>
<td>
JavaScript 1.5

</td>
<td>
Navigator 6.0
 Mozilla (open source browser)

</td>
</tr>
<tr>
<td>
JavaScript 1.6

</td>
<td>
\<a href="mks://localhost/en/Firefox\_1.5\_for\_developers" title="en/Firefox\_1.5\_for\_developers"\>Firefox 1.5\</a\>, other Mozilla 1.8-based products

</td>
</tr>
<tr>
<td>
JavaScript 1.7

</td>
<td>
\<a href="mks://localhost/en/Firefox\_2\_for\_developers" title="en/Firefox\_2\_for\_developers"\>Firefox 2\</a\>, other Mozilla 1.8.1-based products

</td>
</tr>
<tr>
<td>
JavaScript 1.8

</td>
<td>
\<a href="mks://localhost/en/Firefox\_3\_for\_developers" title="en/Firefox\_3\_for\_developers"\>Firefox 3\</a\>, other Gecko 1.9-based products

</td>
</tr>
\</tbody\>

</table>
Each version of the Netscape Enterprise Server also supports a different version of JavaScript. To help you write scripts that are compatible with multiple versions of the Enterprise Server, this manual uses an abbreviation to indicate the server version in which each feature was implemented.

<table class="standard-table">
<caption style="text-align: left;">
Table 2 Abbreviations of Netscape Enterprise Server versions

</caption>
\<thead\>

<tr>
<th scope="col">
Abbreviation

</th>
<th scope="col">
Enterprise Server version

</th>
</tr>
\</thead\> \<tbody\>

<tr>
<td>
NES 2.0

</td>
<td>
Netscape Enterprise Server 2.0

</td>
</tr>
<tr>
<td>
NES 3.0

</td>
<td>
Netscape Enterprise Server 3.0

</td>
</tr>
\</tbody\>

</table>
## Where to find JavaScript information

JavaScript documentation includes the following books:

-   \<a href="mks://localhost/en/JavaScript/Guide" title="en/Core\_JavaScript\_1.5\_Guide"\>JavaScript Guide\</a\> (this guide) provides information about JavaScript language and its objects.
-   \<a href="mks://localhost/en/JavaScript/Reference" title="en/JavaScript/Reference"\>JavaScript Reference\</a\> provides reference material for JavaScript language.

If you are new to JavaScript, start with the \<a href="mks://localhost/en/JavaScript/Guide" title="en/Core\_JavaScript\_1.5\_Guide"\>JavaScript Guide\</a\>. Once you have a firm grasp of the fundamentals, you can use the \<a href="mks://localhost/en/JavaScript/Reference" title="en/JavaScript/Reference"\>JavaScript Reference\</a\> to get more details on individual objects and statements.

## Tips for learning JavaScript

Getting started with JavaScript is easy: all you need is a modern Web browser. This guide includes some JavaScript features which are only currently available in the latest versions of Firefox (and other Gecko powered browsers), so using the most recent version of Firefox is recommended.

### An interactive interpreter

An interactive JavaScript prompt is an invaluable aid to learning the language, as it enables you to try things out interactively without having to save a file and refresh a page. The Firefox Error Console, accessible through the Tools menu, provides a simple way to try interactive JavaScript: Just enter a line of code and click the "Evaluate" button.

\<img alt="Image:ErrorConsole.png" class="internal" src="/@api/deki/files/192/=ErrorConsole.png" /\>

### Firebug

A more advanced interactive prompt is available using \<a class="external" href="<http://www.getfirebug.com/>"\>Firebug\</a\>, a Firefox extension. Expressions you type are interpreted as objects and linked to other parts of Firebug. For example, you can add 5 plus 5, change the case of a string, get a clickable link to the document, or get a link to an element:

\<img alt="" class="internal" src="/@api/deki/files/5188/=FirebugCommandLine.PNG" style="width: 728px; height: 281px;" /\>

Using the arrow on the right bottom corner gives a command editor for multiline scripts.

Firebug also provides an advanced DOM inspector, a JavaScript debugger, a profiling tool and various other utilities. JavaScript code running in a Web page can call, `console.log()`, a function that prints its arguments to the Firebug console.

Many of the examples in this guide use `alert()` to show messages as they execute. If you have Firebug installed you can use `console.log()` in place of `alert()` when running these examples.

## Document conventions

JavaScript applications run on many operating systems; the information in this book applies to all versions. File and directory paths are given in Windows format (with backslashes separating directory names). For Unix versions, the directory paths are the same, except that you use slashes instead of backslashes to separate directories.

This guide uses uniform resource locators (URLs) of the following form:

`http://server.domain/path/file.html`

In these URLs, *server* represents the name of the server on which you run your application, such as `research1` or `www`; *domain* represents your Internet domain name, such as `netscape.com` or `uiuc.edu`; *path* represents the directory structure on the server; and *file*`.html` represents an individual file name. In general, items in italics in URLs are placeholders and items in normal monospace font are literals. If your server has Secure Sockets Layer (SSL) enabled, you would use `https` instead of `http` in the URL.

This guide uses the following font conventions:

-   `The monospace font` is used for sample code and code listings, API and language elements (such as method names and property names), file names, path names, directory names, HTML tags, and any text that must be typed on the screen. (`Monospace italic font` is used for placeholders embedded in code.)
-   *Italic type* is used for book titles, emphasis, variables and placeholders, and words used in the literal sense.
-   **Boldface** type is used for glossary terms.

``` js
autoPreviousNext("JSGChapters");
```

* * * * *

**CC-BY-SA Licensed Work**
 Copyright 2012 Mozilla Contributors. This article contains work licensed under the [Creative Commons Attribution-Sharealike License v2.5](http://creativecommons.org/licenses/by-sa/2.5/) or later. The original work is available at [Mozilla Developer Network](https://developer.mozilla.org): [About this guide](https://developer.mozilla.org/en/JavaScript/Guide/About).

* * * * *
