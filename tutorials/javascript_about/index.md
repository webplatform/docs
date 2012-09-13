{{Flags
|Content=Outdated, Not Neutral
|Compatibility=Outdated, Incomplete
|Editorial notes=The table that maps JavaScript versions to Navigator/Firefox versions could be expanded to include other browsers, or just deleted. The table of NES versions should be deleted.
}}
{{Summary_Section|JavaScript is a cross-platform, object-based scripting language. This guide explains everything you need to know about using JavaScript.}}
{{Guide
|Content=== New features in JavaScript versions ==

* New in JavaScript 1.5
* New in JavaScript 1.6
* New in JavaScript 1.7
* New in JavaScript 1.8
* New in JavaScript 1.8.1
* New in JavaScript 1.8.5

== What you should already know ==

This guide assumes you have the following basic background:

* A general understanding of the Internet and the World Wide Web (WWW).
* Good working knowledge of HyperText Markup Language ([[/html|HTML]]).

Some programming experience with a language such as C or Visual Basic is useful, but not required.

== JavaScript versions == 
'''Table 1: JavaScript and Navigator versions'''

{|
|'''JavaScript version''' || '''Navigator version'''
|JavaScript 1.0 || Navigator 2.0
|JavaScript 1.1 || Navigator 3.0
|JavaScript 1.2 || Navigator 4.0-4.05
|JavaScript 1.3 || Navigator 4.06-4.7x
|JavaScript 1.4 ||	 
|JavaScript 1.5 || Navigator 6.0, Mozilla (open source browser)
|JavaScript 1.6 || Firefox 1.5, other Mozilla 1.8-based products
|JavaScript 1.7 || Firefox 2, other Mozilla 1.8.1-based products
|JavaScript 1.8 || Firefox 3, other Gecko 1.9-based products
|}

Each version of the Netscape Enterprise Server also supports a different version of JavaScript. To help you write scripts that are compatible with multiple versions of the Enterprise Server, this manual uses an abbreviation to indicate the server version in which each feature was implemented.

'''Table 2 Abbreviations of Netscape Enterprise Server versions'''
{|
|'''Abbreviation'''|| '''Enterprise Server version'''
|NES 2.0 || Netscape Enterprise Server 2.0
|NES 3.0 || Netscape Enterprise Server 3.0
|}

== Where to find JavaScript information ==
JavaScript documentation includes the following books:

* [[/guides/JavaScript|JavaScript Guide]] (this guide) provides information about JavaScript language and its objects.
* [[/js | JavaScript Reference]] provides reference material for the JavaScript language.

If you are new to JavaScript, start with the JavaScript Guide. Once you have a firm grasp of the fundamentals, you can use the JavaScript Reference to get more details on individual objects and statements.

== Tips for learning JavaScript ==
Getting started with JavaScript is easy: all you need is a modern Web browser. This guide includes some JavaScript features which are only currently available in the latest versions of Firefox (and other Gecko powered browsers), so using the most recent version of Firefox is recommended.

=== An interactive interpreter ===

An interactive JavaScript prompt is an invaluable aid to learning the language, as it enables you to try things out interactively without having to save a file and refresh a page. The Firefox Error Console, accessible through the Tools menu, provides a simple way to try interactive JavaScript: Just enter a line of code and click the "Evaluate" button.

=== Firebug ===

A more advanced interactive prompt is available using Firebug, a Firefox extension. Expressions you type are interpreted as objects and linked to other parts of Firebug. For example, you can add 5 plus 5, change the case of a string, get a clickable link to the document, or get a link to an element:

Using the arrow on the right bottom corner gives a command editor for multiline scripts.

Firebug also provides an advanced DOM inspector, a JavaScript debugger, a profiling tool and various other utilities. JavaScript code running in a Web page can call, console.log(), a function that prints its arguments to the Firebug console.

Many of the examples in this guide use alert() to show messages as they execute. If you have Firebug installed you can use console.log() in place of alert() when running these examples.

== Document conventions ==

JavaScript applications run on many operating systems; the information in this book applies to all versions. File and directory paths are given in Windows format (with backslashes separating directory names). For Unix versions, the directory paths are the same, except that you use slashes instead of backslashes to separate directories.

This guide uses uniform resource locators (URLs) of the following form:

<code>http://''server.domain/path/file''.html</code>

In these URLs, ''server'' represents the name of the server on which you run your application, such as <code>research1</code> or <code>www</code>; <code>domai</code> represents your Internet domain name, such as example.com; ''path'' represents the directory structure on the server; and ''file''.html represents an individual file name. In general, items in italics in URLs are placeholders and items in normal monospace font are literals. If your server has Secure Sockets Layer (SSL) enabled, you would use <code>https</code> instead of <code>http</code> in the URL.

This guide uses the following font conventions:

* The <code>monospace font</code> is used for sample code and code listings, API and language elements (such as method names and property names), file names, path names, directory names, HTML tags, and any text that must be typed on the screen. (Monospace italic font is used for placeholders embedded in code.)
* ''Italic'' type is used for book titles, emphasis, variables and placeholders, and words used in the literal sense.
* '''Boldface''' type is used for glossary terms.
}}
{{See_Also_Section}}
{{Topics|JavaScript}}
{{External_Attribution
|Is_CC-BY-SA=Yes
|Sources=MDN
|MDN_link=https://developer.mozilla.org/en-US/docs/JavaScript/Guide/About
|MSDN_link=
|HTML5Rocks_link=
}}