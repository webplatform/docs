---
title: 'The basics of HTML'
tags:
  - Tutorials
  - WSC
  - HTML
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - HTML
    - 'The history of the Web'
    - 'The web standards model - HTML CSS and JavaScript'
    - HTML/Elements/head
    - 'The HTML head element'
    - HTML/Elements/title
    - HTML/Elements/body
    - 'HTML/Elements/h1, h2, h3, h4, h5, and h6'
uri: 'tutorials/The basics of HTML'

---
## Introduction

In this article in the Web Standards Curriculum series, you will learn the basics of HTML—what it is, what it does, its history in brief, and what the structure of an HTML document looks like. The articles that follow this one will look at each individual part of HTML in much greater depth.

## What HTML is

Most desktop applications that read and write files use a special file format. For example, Microsoft Word understands “.doc” files and Microsoft Excel understands “.xls”. These files contain the instructions on how to rebuild the documents next time you open them, what the contents of that document are, and “metadata” about the article such as the author, the date the document was last modified, even things such a list of changes made so you can go back and forth between versions.

[HTML](/w/index.php?title=HTML&action=edit&redlink=1) (“HyperText Markup Language”) is a language to describe the contents of web documents. It uses a special syntax containing markers (called “elements”) which are wrapped around the text within the document to indicate how user agents (eg. web browsers) should interpret that portion of the document.

A user agent is any software that is used to access web pages on behalf of users. There is an important distinction to be made here—all types of desktop browser software (Internet Explorer, Opera, Firefox, Safari, Chrome etc.) and alternative browsers for other devices (such as the Wii Internet channel, and mobile phone browsers such as Opera Mini and WebKit on the iPhone) are user agents, but not all user agents are browser software. The automated programs that Google and Yahoo! use to index the web to use in their search engines are also user agents, but no human being is controlling them directly.

## What HTML looks like

HTML is just a plain textual representation of content and its general meaning. For example:

\<p id="example"\>This is a paragraph.\</p\>

The “`<p>`” part is a marker (which we refer to as a “tag”) that means “what follows should be considered as a paragraph”. Because it is at the start of the content it is affecting, this particular tag is an "opening tag". The “`</p>`” is a tag to indicate where the end of the paragraph is (which we refer to as a “closing tag”). The opening tag, closing tag and everything in between is called an “element”. The `id="example"` is an attribute; you'll learn more about these later on. Many people use the terms element and tag interchangeably however, which is not strictly correct.

In most browsers there is a “Source” or “View Source” option, commonly under the “View” menu. Try this now - go to your favourite web site, choose this option, and spend some time looking at the HTML that makes up the structure of the page.

## The history of HTML

In the article [The history of the Internet and the web, and the evolution of web standards](/w/index.php?title=The_history_of_the_Web&action=edit&redlink=1) you learned a little about how the modern Web came about. When Tim Berners-Lee invented the World Wide Web, he created both the first web server and web browser and [the first version of HTML](http://www.w3.org/History/19921103-hypertext/hypertext/WWW/MarkUp/MarkUp.html).

Whilst HTML has changed considerably since the first days, a lot of the content of modern-day HTML is embodied in that first documentation and more than half of the “tags” described in the original “HTML tags” document still exist.

As more people started writing web pages and alternatives to the original browser software, more features were added to HTML. Many were adopted universally (such as the `img` element used to insert an image into a document, first implemented in NCSA Mosaic). Some were more proprietary and really only used in one or two browsers. There was a growing need for standardisation — so that web developers and authors of web browsing software had a document (called a “specification”) that definitively described to them what HTML looked like so they could judge whether they were implementing/using HTML correctly.

The [IETF](http://www.ietf.org/) (Internet Engineering Task Force — a standards body concerned with inter-operability across the internet) published a draft proposal of HTML in 1993. This expired without becoming a standard in 1994, but prompted the IETF to create a working group to look at HTML standardisation.

In 1995, HTML 2.0 was written, taking ideas from the original HTML draft. An alternate proposal called HTML+ was also written by Dave Raggett, which was used as a basis for many of the new elements implemented by browsers (such as the method for inserting images into documents, pioneered by NCSA Mosaic).

A draft of HTML 3.0 followed later that year, but work on that version was discontinued because of a lack of support for the direction from browser makers. HTML 3.2 dropped many of the new features of 3.0, and instead adopted many of the creations of the then-popular browsers Mosaic and Netscape Navigator.

In 1997, the W3C published HTML 4.0 as a recommendation that adopted more browser-specific extensions but also attempted to rationalize and clean up HTML. This was done by marking various elements as deprecated—which means the elements are obsolete and whilst they still exist in this version they will be removed in a later revision. This was to encourage better and more semantic use of HTML in documents (described in more detail our [The web standards model](/w/index.php?title=The_web_standards_model_-_HTML_CSS_and_JavaScript&action=edit&redlink=1)).

HTML 4.01 was published in 1999, with some errata noted in 2001. This is the latest version of HTML, although HTML 5 is currently being drafted.

In 2000, the W3C also published the XHTML 1.0 specification, which was HTML re-structured to be a valid XML document.

In 2007, the W3C restarted the work on HTML by creating a new working group and adopting the work started by the [WhatWG](http://whatwg.org/) as HTML5. In this course we will be using HTML5, but don't worry — if you have already done some work in HTML4, you won't need to relearn everything. HTML5 contains all of HTML4 (albeit with some features redefined), and also adds some new powerful features on top. We'll make it clear when something we are talking about is new in HTML5.

## The structure of an HTML document

A typical example HTML document looks like so:

``` html
<!DOCTYPE html>
<html>
  <head>
    <title>Example page</title>
  </head>
  <body>
    <h1>Hello world</h1>
  </body>
</html>
```

 This looks like so when rendered in a web browser:

![HTMLrender.png](//static.webplatform.org/a/ab/HTMLrender.png)

The document first starts with a document type element, or doctype. This mainly serves to get the browser to render the HTML in what is called "standards mode", so it will work correctly. It also lets validation software know what version of HTML to validate your code against. Don't worry too much about what this all means for now. We will come back to this later. What you can see here is the HTML5 doctype.

After this, you can see the opening tag of the `html` element. This is a wrapper around the entire document. The closing `html` tag is the last thing in any HTML document.

Inside the `html` element, there is the `head` element. This is a wrapper to contain information about the document (the metadata). This is described in more detail in [The HTML head element](/w/index.php?title=The_HTML_head_element&action=edit&redlink=1). Inside the head is the `title` element, which defines the “Example page” heading in the menu bar.

After the `head` element there is a `body` element, which is the wrapper to contain the actual content of the page—in this case, only a level-one header (`h1`) element, which contains the text “Hello world.”

And that’s our document in full.

Elements often contain other elements. The body of the document will invariably end up involving many nested elements. Structural elements such as `article`, `header` and `div` create the overall structure of the document, and will contain subdivisions. These will contain headings, paragraphs, lists and so on. Paragraphs can contain elements that make links to other documents, quotes, emphasis and so on. You will find out more about these elements in later articles.

## The syntax of HTML elements

A basic element in HTML consists of two markers around a block of text, and in almost every case elements can contain sub-elements (such as `html` containing `head` and `body` in the example above). There are some exceptions to the rule: some elements do not contain text or sub-elements, for example `img`. You'll learn more about these later on.

Elements can also have attributes, which can modify the behaviour of the element and introduce extra meaning. Let's have a look at another example.

    <header>
      <h1>The Basics of
        <abbr title="Hypertext Markup Language">HTML</abbr>
      </h1>
    </header>

This looks like so when rendered:

![htmlrender2.png](//static.webplatform.org/7/71/htmlrender2.png)

In this example a `header` element (used to mark up header sections of documents) contains an `h1` element (first, or most important level header), which in turn contains some text. Part of that text is wrapped in an `abbr` element (used to specify the expansion of abbreviations), which has a `title` attribute, the value of which is set to `Hypertext Markup Language`.

Many attributes in HTML are common to all elements, though some are specific to a given element or elements. They are always of the form `keyword="value"`. The value is often surrounded by single or double quotes: this is not necessary in HTML5, except when the attribute value has multiple words, in which case you need to use quotes to make it clear that it is a single attribute value, and not several attributes. Saying all this, I would however recommend that you stick to quoting values for now, as it is good practice and can make the code easier to read. In addition, some HTML flavours you may work with in the future DO require quoting of attributes, for example XHTML 1.0, and it doesn't hurt to do so in flavours that don't.

[Attributes and their possible values are mostly defined by the HTML specifications](http://www.w3.org/TR/html401/index/attributes.html)—you cannot make up your own attributes without making the HTML invalid, as this can confuse user agents and cause problems interpreting the web page correctly. The only real exceptions are the `id` and `class` attributes—their values are entirely under your control, as they are for defining custom meanings .

An element within another element is referred to as being a “child” of that element. So in the above example, `abbr` is a child of the `h1`, which is itself a child of the `header`. Conversely, the `header` element would be referred to as a “parent” of the `h1` element. This parent/child concept is important, as it forms the basis of CSS and is heavily used in JavaScript.

## Block level and inline elements

There are two general categories of elements in HTML, which correspond to the types of content and structure those elements represent—block level elements and inline elements.

Block level means a higher level element, normally informing the structure of the document. It may help to think of block level elements being those that start on a new line, breaking away from what went before. Some common block level elements include paragraphs, list items, headings and tables.

Inline elements are those that are contained within block level structural elements and surround only small parts of the document’s content, not entire paragrahs and groupings of content. An inline element will not cause a new line to appear in the document: they are the kind of elements that would appear in a paragraph of text. Some common inline elements include hypertext links, highlighted words or phrases and short quotations.

Note: HTML5 redefines the element categories in HTML5: see [Element content categories](http://www.whatwg.org/specs/web-apps/current-work/complete/section-index.html#element-content-categories). While these definitions are more accurate and less ambiguous than the ones that went before, they are a lot more complicated to understand than "block" and "inline". We will therefore stick with these throughout this course.

## Character references

One last item to mention in an HTML document is how to include special characters. In HTML the characters `<`, `>` and `&` are special. They start and end parts of the HTML document, rather than representing the characters less-than, greater-than and ampersand.

One of the earliest mistakes a web author can make is to use an ampersand in a document and then have something unexpected appear. For example, writing “Imperial units measure weight in stones&pounds” could actually end up appearing as “…stones£s” in some browsers.

This is because the literal string “&pound;” is actually a character reference in HTML. A character reference is a way of including a character into a document that is difficult or impossible to enter using a keyboard, or in a particular document encoding.

The ampersand (&) introduces the reference and the semi-colon (;) ends it. However, many user agents can be quite forgiving of HTML mistakes such as leaving out the semi-colon, and treat “&pound” as a character reference. References can either be numbers (numeric references) or shorthand words (entity references).

An actual ampersand has to be entered into a document as "&amp;", which is the character entity reference, or as "&\#38;" which is the numeric reference. [A full chart of character references can be found on evolt.org](http://www.evolt.org/article/A_Simple_Character_Entity_Chart/17/21234/).

## Summary

In this article, you have learned the basics of HTML, where it has evolved from and have some insight into the structure of an HTML document. We will now continue to describe the `head` section of an HTML document in some more detail, before continuing to address the `body` content.

Note: This material was originally published as part of the Opera Web Standards Curriculum, available as 12: The basics of HTML, written by Mark Norman Francis. Like the original, it is published under the Creative Commons Attribution, Non Commercial - Share Alike 2.5 license.
