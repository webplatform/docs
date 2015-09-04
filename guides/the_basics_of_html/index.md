---
title: the basics of html
tags:
  - Guides
  - HTML
readiness: 'Ready to Use'
summary: "In this article, you will learn the basics of HTML and gain some insight into the structure and content of an HTML\ndocument.\n"
uri: 'guides/the basics of html'
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - 'guides/the basics of html/af'
    - 'guides/the basics of html/ar'
    - 'guides/the basics of html/ast'
    - 'guides/the basics of html/az'
    - 'guides/the basics of html/bcc'
    - 'guides/the basics of html/bg'
    - 'guides/the basics of html/br'
    - 'guides/the basics of html/ca'
    - 'guides/the basics of html/cs'
    - 'guides/the basics of html/da'
    - 'guides/the basics of html/de'
    - 'guides/the basics of html/diq'
    - 'guides/the basics of html/el'
    - 'guides/the basics of html/eo'
    - 'guides/the basics of html/fa'
    - 'guides/the basics of html/fi'
    - 'guides/the basics of html/fr'
    - 'guides/the basics of html/gl'
    - 'guides/the basics of html/gu'
    - 'guides/the basics of html/he'
    - 'guides/the basics of html/hu'
    - 'guides/the basics of html/hy'
    - 'guides/the basics of html/id'
    - 'guides/the basics of html/it'
    - 'guides/the basics of html/ka'
    - 'guides/the basics of html/kk'
    - 'guides/the basics of html/km'
    - 'guides/the basics of html/ksh'
    - 'guides/the basics of html/kw'
    - 'guides/the basics of html/mk'
    - 'guides/the basics of html/ml'
    - 'guides/the basics of html/mr'
    - 'guides/the basics of html/ms'
    - 'guides/the basics of html/nl'
    - 'guides/the basics of html/no'
    - 'guides/the basics of html/oc'
    - 'guides/the basics of html/pl'
    - 'guides/the basics of html/pt'
    - 'guides/the basics of html/pt-br'
    - 'guides/the basics of html/ro'
    - 'guides/the basics of html/ru'
    - 'guides/the basics of html/si'
    - 'guides/the basics of html/sk'
    - 'guides/the basics of html/sl'
    - 'guides/the basics of html/sq'
    - 'guides/the basics of html/sr'
    - 'guides/the basics of html/ta'
    - 'guides/the basics of html/th'
    - 'guides/the basics of html/tr'
    - 'guides/the basics of html/uk'
    - 'guides/the basics of html/vi'
    - 'guides/the basics of html/yue'
    - 'guides/the basics of html/zh'
    - 'guides/the basics of html/zh-hans'
    - 'guides/the basics of html/zh-hant'
    - 'guides/the basics of html/zh-tw'

---
# The Basics of HTML

## Summary

In this article, you will learn the basics of HTML and gain some insight into the structure and content of an HTML document.

## Introduction

This article summarises the purpose and structure of HTML in a very high-level fashion, including how elements work, and what character references are. The articles that follow will go into more detail on specific parts of the HTML language.

## What is HTML?

Most desktop applications that read and write files use specific file formats. For example, Microsoft Word uses ".doc" files and Microsoft Excel uses ".xls". These files contain the instructions on how to build the documents when they are opened, the contents of the document, and *metadata* about the document such as the author, the last modified date, and possibly even a list of changes.

[HTML (*HyperText Markup Language*)](/html) is a language used to describe the contents of web documents. It uses a syntax containing markers (called *elements*) that are wrapped around content in the document to indicate how user agents (e.g., web browsers) should interpret that portion of the document.

A *user agent* is any software that is used to access web pages on behalf of users. There is an important distinction to be made here — all types of desktop browsers (such as Internet Explorer, Opera, Firefox, Safari, and Chrome) as well as alternative browsers for other devices (such as the Wii Internet channel, and mobile phone browsers like Opera Mini and WebKit on the iPhone) are user agents, but not all user agents are browsers. For example, the automated programs that Google and Yahoo! use to index the web for their search engines are user agents, but no human being is controlling them directly.

## What HTML looks like

HTML is a plain textual representation of content and its general meaning. For example:

``` {.html}
<p id="example">This is a paragraph.</p>
```

 The `<p>` part is a marker, commonly called a *tag*, that means "what follows should be considered as a paragraph". Because it is at the start of the content it affects, it is an "opening tag". Likewise, the `</p>` tag indicates the end of the paragraph, and is thus a "closing tag". The opening tag, closing tag, and everything in between is called an *element*. Note: Many people use the terms "element" and "tag" interchangeably, which is incorrect. (The `id="example"` is an *attribute-value pair*; we'll come back to these later.)

In most browsers there is a "Source" or "View Source" option, commonly under the "View" menu. Try this now: go to a web site, choose this option, and spend some time looking at the HTML that makes up the page.

## The structure of an HTML document

A typical HTML document might look like this:

``` {.html}
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <title>Example page</title>
  </head>
  <body>
    <h1>Hello world</h1>
  </body>
</html>
```

 That document might look like this when rendered in a web browser:

![HTMLrender.png](/assets/public/a/ab/HTMLrender.png)

The document starts with a document type element, or *doctype*, in this case the HTML5 doctype. This mainly serves to get the browser to render the HTML in what is called "standards mode", so it will work correctly. It also lets validation software know what version of HTML to validate your code against.

Next, you can see the opening tag of the `<html>` element. This is a wrapper around the entire document. The closing `</html>` tag is the last thing in any HTML document. The `html` element should always have a `lang` attribute. This specifies the primary language for the page. For example, `en` means "English", `fr` means "French". There are tools available to help you find the right language tag, such as Richard Ishida's [Language Subtag Lookup tool](http://rishida.net/utils/subtags/).

Inside the `html` element, there is the `head` element. This is a wrapper that contains other information about the document such as internal or external styles and scripts. This is described in more detail in [The HTML head element](/html/elements/head). Inside the `head` is the `title` element, which defines the "Example page" heading in the brower's title bar. The `head` element should always contain a `meta` element with a `charset` attribute that identifies the character encoding of the page. (The one exception is when the page is encoded in UTF-16, but you should avoid that encoding anyway.) You should use UTF-8 whenever possible. See [this W3C article](http://www.w3.org/International/getting-started/characters) for more about character encodings.

After the `head` element there is a `body` element, which is the wrapper that surrounds the actual content of the page — in this case, a level-one heading (`h1`) element, which contains the text "Hello world".

And that's our document in full.

## The syntax of HTML elements

A basic element in HTML consists of two markers around a block of content. Elements also often contain other elements, referred to as *nested elements*. The body of a document invariably contains many nested elements. Structural elements such as `article`, `header`, and `div` create the overall structure of the document, and will themselves contain headings, paragraphs, lists, and other elements. Paragraphs can contain elements that create links to other documents, quotes, emphasis, and so on. Nearly any element can contain nested elements, although there are exceptions: some elements do not contain either text or nested elements, for example `img`.

An element within another element is also referred to as a "child" element. So in the below example, `abbr` is a child of `h1`, which is itself a child of `header`. Conversely, the `header` element would be referred to as the "parent" of the `h1` element, which is the parent of `abbr`. This parent/child concept is important, as it forms the basis of CSS (Cascading Stylesheet Specification) and is heavily used in JavaScript.

Elements can also have attributes, which can modify the appearance and/or behaviour of the element and introduce extra meaning. Let's look at another example.

``` {.html}
<header>
  <h1>The Basics of
    <abbr title="Hypertext Markup Language">HTML</abbr>
  </h1>
</header>
```

 This looks like so when rendered in a browser:

![htmlrender2.png](/assets/public/7/71/htmlrender2.png)

In this example, a `header` element contains an `h1` heading element, which in turn contains some text. Part of that text is wrapped in an `abbr` element (used to specify the expansion of abbreviations), which has a `title` attribute, the value of which is `Hypertext Markup Language`.

Many attributes in HTML are common to all elements, though some are specific to certain elements. They are always of the form `keyword="value"`. The value is often surrounded by single or double quotes. While this is not required in HTML5 (except when the attribute value has multiple words separated by white space), you should always quote values, as it is good practice and can make the code easier to read. In addition, some HTML dialects do require quoting of attributes, for example XHTML 1.0, and it doesn't hurt to do so in dialects that don't require it.

Attributes and their possible values are mostly defined by the [W3C HTML specifications](http://www.w3.org/TR/html401/index/attributes.html). You cannot make up your own attributes without invalidating the HTML, and this can confuse user agents and cause problems interpreting the web page correctly.

## Block and inline elements

There are two general categories of elements in HTML, which correspond to the types of content and structure they represent: *block* elements and *inline* elements.

Block elements are at a higher level, normally helping to define the structure of the document. It may help to think of block elements as those that start on a new line, breaking away from the previous content. Some common block level elements include paragraphs, lists, headings, and tables.

Inline elements are are contained within block elements and typically surround only small parts of the document's content. Inline elements do not cause a new line to appear in the document; rather, they appear inside a line of text. Some common inline elements include hypertext links, bold or italic text, spans, and short quotations.

Note: HTML5 redefines the element categories in HTML: see [Element content categories](http://www.whatwg.org/specs/web-apps/current-work/complete/section-index.html#element-content-categories). While these definitions are more accurate and less ambiguous, they are more difficult to understand than "block" and "inline". We will therefore stick with these terms in this course.

## Character references

One last item to mention in an HTML document is how to include special characters. In HTML the characters `<`, `>` and `&` are special. They start and end parts of the HTML document, rather than representing the printable less-than, greater-than, and ampersand characters. For this reason they must always be coded in a special way in document content.

One of the easiest mistakes to make in a web page is to use \< and \> signs in text and have the browser render your content in an unexpected way. For example, if you write "The paragraph tag (\<p\>) is very common.", intending for it to look just like that, the browser will render it as

The paragraph tag (

) is very common.

This is clearly not what you wanted or expected.

The solution to this problem is to encode, or "escape", the two signs by representing them with character references. The character reference for less-than is "&lt;", and the character reference for greater-than is "&gt;". Thus, to get that line to look the way you want, you would write "The paragraph tag (&lt;p&gt;) is very common", which the browser would render as "The paragraph tag (\<p\>) is very common", as you intended. In these encodings, the ampersand (&) starts the reference and the semicolon (;) ends it.

Character references can also be numeric. For example, you can escape an ampersand character with either its shorthand word `&amp;` or its numeric reference `&#38;`.

Web Platform Docs includes a [Table of Common HTML Entities](/html/entities#HTML_Entities_Table) for reference.

Other than these characters, you should try to avoid using character references unless you are dealing with an invisible or ambiguous character. If you use the UTF-8 character encoding you can represent any character (other than those mentioned above) without escaping them.

For more information about working with character escapes, see [Using character escapes in markup and CSS](http://www.w3.org/International/questions/qa-escapes).

**Language:**
:   ****English****  • <span lang="es">[español](/guides/the_basics_of_html/es)</span> • <span lang="ja">[日本語](/guides/the_basics_of_html/ja)</span> • <span lang="ko">[한국어](/guides/the_basics_of_html/ko)</span> • <span lang="sv">[svenska](/guides/the_basics_of_html/sv)</span>

