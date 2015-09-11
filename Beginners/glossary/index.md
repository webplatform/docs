---
title: Glossary of terms
readiness: 'Ready to Use'
summary: 'This page provides basic definitions of fundamental web technologies, concepts and other terms you might meet while learning web development.'
tags:
  - Basic
  - Pages
uri: Beginners/glossary

---
## <span>Summary</span>

This page provides basic definitions of fundamental web technologies, concepts and other terms you might meet while learning web development.

## <span>Beginners submenu</span>

The **[Beginners](/Beginners)** section covers the various aspects of web development separated in 9 parts, you can navigate through them using this list.

-   [1. The beginning](/Beginners/the_beginning)
-   [2. A crash course in web site code](/Beginners/crash_course)
-   [3. Planning](/Beginners/planning)
-   [4. Structuring our content with HTML](/Beginners/html)
-   [5. Styling our content with CSS](/Beginners/css)
-   [6. Programming fundamentals](/Beginners/programming)
-   [7. JavaScript](/Beginners/javascript)
-   [8. Advanced topics](/Beginners/advanced)
-   [9. Browser testing](/Beginners/browser_testing)
-   **Glossary**

## <span>Terms</span>

### <span>Alignment</span>

The horizontal or vertical positioning of an element. Typical horizontal alignments include left, right, and center; typical vertical alignments include baseline, sub, super, top, text-top, middle, bottom, and text-bottom.

### <span>API (Application Program Interface)</span>

A set of commands, functions, and protocols which can be used to build websites. APIs are predefined functions that web site authors can call to perform certain tasks instead of writing code from scratch to perform them.

### <span>Attribute</span>

An instruction or definition or additional defined characteristic of an Element, such as `href` or `title`, the parts that show up to the left of equal signs after the Element itself in the opening tag, thus

``` html
<tag href="#" title="the href and title are what we call attributes">Tag content</tag>
```

**Note**: Historically everybody was writing tags with *Capital letters*. Nowadays, we write both tag names and their attribute names in lowercase. The web browser doesn’t make a difference how you write your tag names and attributes, but its a common convention that many web developers adopted during the epoch just before we started using HTML5.

### <span>Border</span>

The edge delimiting the boundaries of an element box.

### <span>Browser</span>

A program installed on a Client allowing it to access and display web sites, thereby allowing you to interact with the Web. CSS (Cascading Style Sheets): A language for specifying how documents are presented to users. A document is a collection of information that is structured using a markup language.

### <span>Client</span>

Any computing device, such as your laptop or mobile phone, that can be used to connect to and draw content from the web. Your device uses an application (usually a web browser) to request a web site/other data from a server; the server then sends back a response, which includes all the information needed for your application to display the web site or other data you requested. Cursive: Used to describe fonts that have a decorative, often handwritten-looking style

### <span>DNS (Domain Name Server)</span>

This is essentially an address book for the Web that links common names to the numerical addresses at which all Web sites are stored. All Web sites are actually located at numerical addresses of the form \#\#\#.\#\#\#.\#\#\#.\#\#\# called IP addresses. Domain Name Servers associate these addresses with domain names, so they are easier to handle for humans. So for example, the IP address of google.co.uk is 173.194.66.94 — try typing it in and you'll see we're right — but google.co.uk is far easier to remember!

### <span>DOM The Document Object Model (DOM)</span>

An application programming interface (API) for markup documents, like HTML, SVG, MathML, and XML. The DOM provides a logically structured representation of a document, and a set of Objects and Methods for manipulating that structure.

### <span>Element</span>

Or a tag. We basically give a one word (no space), surround it by angle brackets (e.g. \<html\>). There are various types of tags and they depend of their role.

For example, to make a link we surround the text we want to use as the text to click on (i.e. an element), and in other case, we just want to add information without showing information directly (i.e. a self closing tag).

When the documentation refers to an element we are talking about HTML tags that are *inside* the `<body>` tag of a page.

### <span>Entity</span>

If you want to show characters that might not exist, or might also create confusion in the web page, we can still use them in a way that the web browser will understand and convert for you.

The ones to remember are characters we use in an HTML document and if we use them, we might break the validity of the document. The easy to remember ones are: angle brackets (\<\>), amperstand (&), but there are many others we can use.

To tell the web browser we want to display a special character we annotate them in the source. The notation is basically the amperstand symbol (&) and a code. Sometimes we can use an alias instead of the code (easier to remember). When the code has no alias (e.g. amp), we prepend it with a pound sign (\#) and a number based on the ASCII table.

Here are a few examples: ¶ (`&#182;`), ¼ (`&#182;`). Its also possible to use both code and alias notation, for example: & could be shown either by doing `&#38;` or `&amp;`.

### <span>Code</span>

A means for displaying an Entity, such as \< without it having coding effect, typically by use of a string that begins &\#. Fantasy: Used to describe fonts that have a bold, often ornamental or quirky style, which are meant to be used for headings, not body copy

### <span>Font Stack</span>

A sequential listing of preferred fonts to display on a web page allowing a developer to specify alternatives in the case that a desired font is not available to a Client.

### <span>FTP (File Transfer Protocol)</span>

A protocol that defines the manner in which files can be loaded to or from Servers such that there is a standard method that can be used by any of the many disparate devices that can connect to the Web.

### <span>Hexadecimal</span>

While common numbers goes from 0-9 (i.e. decimal numbers). This notation is easy for us, humans, to understand. But it also implies that one numeric charcter slot cannot go higher than 9. In hexadecimal, one slot can go up to 16. This is what we call "base 16" and Hexadecimal is also a common name for this. Hexadecimal numbers goes from 0-9, then uses the alphabet letters A-F to fill the gap.

For example, we use Hexadecimal numbers to describe a color. On computer screens, colors are based on red, green and blue (commonly called RGB). Every color has a percentage of each colors. To obtain red in RGB, we would need: 100% or red, 0% or green, 0% of blue.

In Hexadecimal, we would say that 0% is represented as `00`, and 100% as `FF`.

*NOTE*: Technically two hexadecimal characters can represent 255 possibilities, but in CSS we round it as if it was a percentage value.

Therefore, red in RGB would be described as the string `#FF0000;` in CSS.

### <span>HTML (Hyper Text Markup Language)</span>

A language to describe the contents of web documents. It uses a special syntax containing markers (called “elements”) which are wrapped around the text within the document to indicate how user agents (eg. web browsers) should interpret that portion of the document.

### <span>Justification</span>

The typographical practice of aligning multiple lines of text precisely to one or both of their common margins. Typically referred to in its individual forms as left, right, center, or full justification.

### <span>Margin</span>

The space surrounding an element box; the space between the border and the margin of an adjacent element.

### <span>Monospaced</span>

Used to describe fonts in which every glyph takes up the same space, like in computer code

### <span>Networking Protocols</span>

Agreed upon methods by which computers communicate with each other on a network, allowing the many different types of computers on the Web to talk to each other. The term HTTP, for instance, means Hyper Text Transfer Protocol and tells your browser how to interface with the network to access information stored on the Web.

### <span>Padding</span>

The space between the substance of an element and the edge of the box that surrounds it.

### <span>RGB</span>

Literally, red, green and blue. For our purposes a hexadecimal notation that provides levels for each of the colors red green and blue.

### <span>Sans-serif</span>

"Sans"; meaning without in french, describes fonts that doesn’t have serifs, the small projecting features at the ends of character strokes. Modern convention holds that sans-serif fonts are preferred over serif fonts for online text, while serif fonts are preferred for print. Serif Term used to describe fonts with small small projecting features at the ends of character strokes.

### <span>Server</span>

A computer on which web sites are stored, ready for delivery to those who want to look at them.

### <span>Style Sheeet</span>

A set of instructions for how the content of a markup file should be displayed.

### <span>SVG</span>

A markup language for graphics.

### <span>Transmission Protocols</span>

The various agreed upon methods for transporting data around the Web.

### <span>User Agent</span>

Any software that is used to access web pages on behalf of users. There is an important distinction to be made here—all types of desktop browser software (Internet Explorer, Opera, Firefox, Safari, Chrome etc.) and alternative browsers for other devices (such as the Wii Internet channel, and mobile phone browsers such as Opera Mini and WebKit on the iPhone) are user agents, but not all user agents are browser software. The automated programs that Google and Yahoo! use to index the web to use in their search engines are also user agents, but no human being is controlling them directly.

### <span>Web Browser</span>

See Browser

### <span>Web-safe fonts</span>

The 11 or so fonts that are installed across almost all systems, termed web safe fonts because they are safe for use in your pages. These are: Verdana, Arial, Trebuchet MS (sans-serif); Times New Roman, Georgia (serif); Andale Mono, Courier New (monospaced); Comic Sans (cursive); Impact (fantasy).

### <span>Web Servers</span>

See Server

### <span>Web Technologies</span>

these are the different types of code that web developers use to create web sites, which define things such as the text you want to show on the web page, the styles that text should have, etc. The web browser receives such code from a server and assembles it into a complete web page.

### <span>XML</span>

A markup language for structured documents in general.

### <span>XUL</span>

A markup language for user interfaces in Mozilla Firefox. Note that the trend in most browser vendors are also using HTML/CSS/JavaScript inside the "browser chrome" (See *Browser chrome* below) and thus deprecating XUL.

### <span>Browser chrome</span>

The term browser chrome is used to describe the actual web browser software and user interface components. It is confusing because the term is much older than Google’s own web browser.

### <span>Polyfill</span>

Also called "Shim" is a piece of code that we can add to a web page to support a feature that is not supported yet. The use of a polyfill goes with the use of techniques to detect and load the "shim", ONLY IF the web browser doesn’t pass the test. We call this technique "Progressive enhancement".

