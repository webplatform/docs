---
title: 'xslt'
readiness: 'Ready to Use'
summary: "XSL Transformations (XSLT) is a markup language for transforming XML into other forms of output, such as XML documents, HTML and many other text-based formats. The World Wide Web Consortium maintains the XSLT standard.\n"
tags:
  - Basic
  - Pages
  - XML
uri: xslt

---
## Summary

XSL Transformations (XSLT) is a markup language for transforming XML into other forms of output, such as XML documents, HTML and many other text-based formats. The World Wide Web Consortium maintains the XSLT standard.

## Background

XSLT is the keystone in a trio of languages developed to transform and format XML. Collectively, those languages are known as XSL, or Extensible Stylesheet Language. Each member of the XSL family has a specific role:

-   XSLT, or XSL Transformations, is used to transform XML data into other kinds of output.
-   XPath, or XML Path Language, is used to identify nodes in an XML document for transformation or formatting.
-   XSL-FO, or XSL Formatting Objects, is a presentational language used for formatting XML data, usually for print.

[XSLT 1.0](http://www.w3.org/TR/1999/REC-xslt-19991116) became an official recommendation in 1999. [XSLT 2.0](http://www.w3.org/TR/2007/REC-xslt20-20070123/) became an official recommendation in 2007. The latest [XSLT 3.0 Working Draft](http://www.w3.org/TR/2012/WD-xslt-30-20120710/) was released 10 July 2012.

## XSLT as a Standards-Based Templating Language

Though the usage of XSLT as a web templating language is not commonplace, there are a lot of factors that make it ideal for this purpose.

-   It’s an XML technology. This means native handling of every web feed, every XHTML page, every RDF format, and nearly every API that exists on the web.
-   It’s an open standard. Maintained by the world’s web standards body (W3C), XSLT is widely-used, widely-supported, and well-documented. You won’t have trouble finding resources or getting answers, and once you’ve learned XSLT it can be helpful anywhere XML is used (which is pretty much everywhere).
-   It’s content-driven. Everything you output is directly tied to the data you need to present, meaning your presentation can always be lean and semantic.
-   It’s rule-based. Rules are much more powerful than mixtures of markup and procedural code. They are distinct and self-contained, but can also have complex relationships and interdependencies.
-   It’s flexible. XSLT can output nearly any text-based format there is, even ones that haven’t been invented yet.
-   It’s a complete templating language. With XSLT you can craft an organized, coherent presentation system rather than cobbling pages together out of snippets and tags using scripting languages.

XSLT defines sets of instructions that are used to transform source XML and create some kind of output. A processor starts with some XML content, and as it parses that content, it uses instructions from an XSLT stylesheet to generate some other sort of output.

Many common programming languages are imperative—they issue commands, one after the other. XSLT, on the other hand, is a declarative language. Instead of issuing commands, it simply states what should be done in a given context. It’s rather similar to CSS in that way. Neither language describes a sequence of events or functions. They just say, "When you come across this element, this is how you should style/transform it.”

Templating with this kind of rule-based language takes a different sort of mindset, but it’s actually a much more powerful and flexible approach. A list of commands can only be followed, but rules can have scope and interdependencies, they can cascade, and they can override one another.
