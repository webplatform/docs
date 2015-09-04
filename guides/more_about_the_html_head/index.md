---
title: more about the html head
tags:
  - Tutorials
  - HTML
readiness: 'Ready to Use'
summary: 'This article delves deeper into the possibilities the HTML <head> has to offer, looking at some additional features.'
uri: 'guides/more about the html head'

---
# More about the HTML \<head\>

## Summary

This article delves deeper into the possibilities the HTML \<head\> has to offer, looking at some additional features.

## Introduction

In [the previous article](/guides/the_html_head) you learned about the essential items that go inside the `head` of an HTML document. In this article we'll expand on that information and talk about some lesser used items that you can add to the `head`. By the end of this tutorial you'll know how to collate several HTML documents into a larger multi-part collection, what RSS is all about, and what a *favicon* is and how to use it.

## Document relationships: collating several HTML documents into a collection

Document relationships are a feature of HTML that stems from the origins of the web as a document repository and, as the name says, define how one document relates to another. For example, a relationship can define if a referenced document is the previous or next document in a logical chain, if it is the index to a whole series of documents, and more.

In a sense, you've already done this in the previous article when you applied a style sheet to a document to give it a different look and feel with the `link` element. Referencing a style sheet establishes a relationship between it and the current document, and defines the type of relationship.

``` {.html}
<!DOCTYPE html>
<html lang="en-GB">
<head>
  <meta charset="utf-8">
  <title>Breeding Dogs - Tips about Alsatians</title>
  <link rel="stylesheet" type="text/css" media="screen" href="styles.css">
  <link rel="stylesheet" type="text/css" media="print" href="printstyles.css">
</head>
<body>
</body>
</html>
```

 The relationship of the current document to others is defined in much the same way using the `link` element and the `rel` or `rev` attributes. The `rel` (*relationship*) attribute defines the relationship that the linked document has to the current one, and the `rev` (*reverse relationship*) attribute defines the relationship the current document has to the linked one. Don't worry about the `rev` attribute now; it is a bit confusing, and you will use it rarely, if at all.

There are no mandatory predefined values for the `rel` and `rev` attributes, but there is a taxonomy for `rel` supported by browsers and indexing tools that you should follow under normal circumstances:

-   home: The home document of the current collection
-   index: The index of the current collection
-   contents: The contents list of the current collection
-   search: The search page of the current collection
-   glossary: The glossary of the current collection
-   help: The help page of the current collection
-   first: The first document in current collection
-   previous: The previous document from this one in the logical order of the collection
-   next: The document following this one in the logical order of the collection
-   last: The last document of the current collection
-   up: The document one level up in the hierarchy of the current collection
-   copyright: The copyright information of the current collection
-   author: The information page about the author of the current collection

Frankly, most browsers don't do anything with this information, although some will follow the link and load the document in the background so that it is displayed faster when requested. The notable exception is Opera, which has an extra navigation toolbar you can turn on by selecting `View > Toolbars > Navigation bar` from the menu. When the toolbar is enabled you see the link relationships defined in the document as an extra toolbar. Figure 1 shows the W3C HTML standards document in Opera.

![Screenshot of the Opera browser showing the navigation bar](/assets/public/2/2e/Morehead.png)

*Figure 1: Opera shows the link relationships of the current document in a special navigation toolbar.*

Even though they may not be visibly displayed, it is a good idea to provide a human-readable explanation of what the linked documents are about in a `title` attribute, as the file names alone are not necessarily enough.

Now let's have a look at how link relationships can be used to collate several documents into a collection. The start page of an online course spanning several documents could look like this:

``` {.html}
<!DOCTYPE html>
<html lang="en-GB">
<head>
  <meta charset="utf-8">
  <title>Link relationship example</title>
  <link rel="contents" title="table of contents" href="toc.html">
  <link rel="next" title="next: chapter one" href="chapter1.html">
</head>
<body>
  <h1>Course example</h1>
  <p>This would be the cover page of an article series or course</p>
  <ul>
    <li><a href="chapter1.html" rel="next">Let's start with Chapter One</a></li>
  </ul>
</body>
</html>
```

 The first chapter document would be the following:

``` {.html}
<!DOCTYPE html>
<html lang="en-GB">
<head>
  <meta charset="utf-8">
  <title>Chapter One - Link relationship example</title>
  <link rel="contents" title="Table of Contents" href="toc.html">
  <link rel="home" title="Home Page" href="start.html">
  <link rel="prev" title="previous: Home Page" href="start.html">
  <link rel="next" title="next: Second Chapter" href="chapter2.html">
</head>
<body>
  <h1>Chapter One</h1>
  <p>This would be the chapter one page of an article series or course</p>
  <ul>
    <li><a href="start.html" rev="prev">Back to Start</a></li>
    <li><a href="toc.html" rel="contents">Table of contents</a></li>
    <li><a href="chapter2.html" rel="next">Go on to Chapter Two</a></li>
  </ul>
</body>
</html>
```

 The second chapter would be:

``` {.html}
<!DOCTYPE html>
<html lang="en-GB">
<head>
  <meta charset="utf-8">
  <title>Link relationship example</title>
  <link rel="contents" title="Table of Contents" href="toc.html">
  <link rel="home" title="Home page" href="start.html">
  <link rel="prev" title="previous: first chapter" href="chapter1.html">
</head>
<body>
  <h1>Chapter Two</h1>
  <p>This would be the second chapter page of an article series or course</p>
  <ul>
    <li><a href="chapter1.html" rev="prev">Back to chapter 1</a></li>
    <li><a href="toc.html" rel="contents">Table of contents</a></li>
  </ul>
</body>
</html>
```

 And finally the table of contents:

``` {.html}
<!DOCTYPE html>
<html lang="en-GB">
<head>
  <meta charset="utf-8">
  <title>Table of contents - Link relationship example</title>
  <link rel="home" title="home page" href="start.html">
</head>
<body>
  <h1>Table of contents</h1>
  <ul>
    <li><a href="chapter1.html">Chapter One - about stuff</a></li>
    <li><a href="chapter2.html">Chapter Two - about other stuff</a></li>
  </ul>
  <ul>
    <li><a href="start.html" rel="home">Back to home</a></li>
  </ul>
</body>
</html>
```

 You can use the `rel` and `rev` attributes on links in the document to tell browsers and assistive technology that these anchors correspond with the link relationships. Also, `rel` and `rev` are sometimes used for other purposes such as Microformats, but that is beyond the scope of this article.

## Linking to alternative versions of the document

The option to link to other documents that have a certain relationship to the current document also includes different language versions of the same document, or different formats. You can do both by providing a link with a `rel` attribute value of `alternate`.

### Translations

Translations are a great candidate for document interlinking. It might be that the English language version of a document is very successful, and you would like to provide other language versions to potential international visitors. By linking from the original to the alternate language version, you make it easier for non-English readers to access and promote your content. The following example shows how you can define the other language versions; note the straightforward syntax.

``` {.html}
<!DOCTYPE html>
<html lang="en-GB">
<head>
  <meta charset="utf-8">
  <title>Multiple Languages example</title>
  <link rel="contents" title="table of contents" href="toc.html">
  <link rel="next" title="next: chapter one" href="chapter1.html">
  <link rel="alternate" title="The course in Dutch" type="text/html" hreflang="nl" href="../nl/start.html">
  <link rel="alternate" title="The course in German" type="text/html" hreflang="de" href="../de/start.html">
</head>
<body>
  <h1>Course example</h1>
  <p>This would be the cover page of an article series or course</p>
  <ul>
    <li><a href="chapter1.html" rel="next">Let's start with Chapter One</a></li>
  </ul>
  <ul>
    <li>Other languages:
      <ul>
        <li><a href="../de/start.html" lang="de" hreflang="de">Deutsch</a></li>
        <li><a href="../de/start.html" lang="nl" hreflang="nl">Nederlands</a></li>
      </ul>
    </li>
  </ul>
</body>
</html>
```

 To recap, the `hreflang` attribute on links and anchors defines the human language of the linked document, and the `lang` attribute defines the language of the text inside the element that has this attribute. This is very important for accessibility as text-to-speech software (screen readers) must switch the pronounciation voice from language to language.

### Feeds

There is another type of alternative web page that you'll see a lot as you trawl the web, called *RSS feeds*. These are very popular, especially for documents that change constantly, such as news sites. RSS actually stands for "Rich Site Summary", but is most often characterized today as "Really Simple Syndication".

A feed is a document containing condensed information detailing new additions to your site in chronological order. Users can subscribe to the feed and see what has changed on your site recently without having to visit it. They do this by using feed readers like [Feedly](http://feedly.com/index.html#welcome), [Netvibes](http://www.netvibes.com/), or [Bloglines](http://www.bloglines.com/). Some modern browsers such as Opera and Firefox, and e-mail clients such as Mac Mail or Windows Outlook can also process and display feeds. You can identify web sites that offer feeds by the RSS icon next to the URL, as shown in Figure 2:

![Screenshot of the Opera browser showing a RSS icon in the navigation bar](/assets/public/d/d7/rss-feed-available.gif)

*Figure 2: Opera shows an orange RSS icon next to the location of websites that offer a feed.*

Feed pages are structured using either HTML or an XML format like RSS or Atom, and they are hardly ever generated by hand. Personal publishing systems will usually do that work for you, so all that's required to offer the world a feed of your site is link to the XML document with the correct meta element in the `head` of your document. The following is an excerpt from a blog at [http://wait-till-i.com](http://wait-till-i.com/), and points to the RSS feed.

``` {.html}
<!DOCTYPE html>
<html lang="en-GB">
<head>
  <meta charset="utf-8">
  <link rel="alternate" type="application/rss+xml" title="Wait till I come! RSS Feed" href="http://www.wait-till-i.com/feed/">
  <title>Wait till I come!</title>
</head>
<body>
  <p>Example of an RSS feed</p>
</body>
</html>
```

 Supplying a feed makes sense for content-heavy websites that change often, like blogs or photo sites, and by using a feed reading tool and subscribing to feeds you can significantly reduce your web surfing and research time.

## Making bookmarking more fun — using favicons

If you don't update your site very often, but you have a lot of content and want people to have a visual reminder of your site, you might want to consider using a shortcut icon. Shortcut icons or *favicons* are small images with a file format of `.ico`; if you place one on your web server, you can use it to help your site stand out in users' bookmark lists, as shown in Figure 3:

![Screenshot of bookmark list with icons next to the entries](/assets/public/4/42/bookmarks.gif)

*Figure 3: Favicons next to a bookmark make it easier to remember the site. You can add one using a shortcut-icon meta element.*

Note that most browsers support various image formats for favicons, but if you want to support Internet Explorer you should stick with `.ico` as that is the only format recognized by IE.

The biggest obstacle to adding a shortcut icon is actually creating it in the right format, as not all graphics editors support the `.ico` format. One option is to use the free online tool [genfavicon](http://www.genfavicon.com/). Once you have created a favicon, assigning it to your document is as easy as adding a meta element with a `rel` value of "Shortcut Icon", as shown in the following example:

``` {.html}
<!DOCTYPE html>
<html lang="en-GB">
<head>
  <meta charset="utf-8">
  <title>Shortcut Icon example</title>
  <link rel="Shortcut Icon" href="favicon.ico" type="image/x-icon">
</head>
<body>
  <h1>Example of a shortcut icon</h1>
</body>
</html>
```

 If you open this document in a browser it should show the Opera icon next to the address in the location toolbar. If you bookmark it, the same icon will appear next to the bookmark.

## Conclusion

In this article, we expanded on the HTML `head` section and explored some additional features that can be added to it. If you have not already done so, please see the previous article in this tutorial pair, [The HTML head](/guides/the_html_head).

## See also

### Exercise questions

-   Why does it make sense to define link relationships when they are not displayed?
-   How would you link to a search page?
-   What use is offering a feed to your visitors? What `rel` value do you use to link to one?
-   What do you need to make sure of when you link to documents in other languages?
-   If you open the example documents in a text editor you’ll find another `meta` element we haven’t discussed here with an attribute of `content-type`, and something called `utf-8`. What is `utf-8`?

