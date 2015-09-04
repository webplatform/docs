---
title: html links
tags:
  - Guides
  - HTML
readiness: 'Ready to Use'
summary: 'In this article we provide a basic treatment of HTML anchors, or <a> elements, more commonly known as HTML links.'
uri: 'guides/html links'

---
# HTML links

## Summary

In this article we provide a basic treatment of HTML anchors, or \<a\> elements, more commonly known as HTML links.

## Introduction

In this article you'll learn about one of the most ground-breaking inventions in the history of the Web — links. Links allow the reader of a document to instantly jump from document to document and from server to server. A lot has happened since links were first introduced, but one thing is the same: links are an immensely important part of the web experience and they can make accessing your content easy or hard for your website's visitors, depending on how you use them.

This article explores how to create links that are easy to understand and function in any environment. Further, we'll look at how linking affects your search engine popularity, and you'll get some tips about wording link text.

## What are links?

*Links* are parts of an HTML document that point to other resources — other HTML documents, text files, PDF files, etc. Some links are followed automatically by the browser, created using `<link>` elements (you've already encountered some of these in earlier articles, as when they were used to import CSS files into an HTML document). But generally, when we talk about links we mean those that are created by the page author and are optional for the user to activate. These are called *anchors*, and you add them to the HTML document using the `<a>` element.

## The anatomy of an anchor

You can turn any inline element or text into an HTML link by adding an `<a>` element around it. For example, in the following HTML document, the text "Opera Software" is a link.

``` {.html}
<!DOCTYPE html>

<html lang="en-GB">
<head>
  <meta charset="utf-8">
  <title>Link Example</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <h1>A link to Opera</h1>
  <p><a href="http://www.opera.com">Opera Software</a></p>
</body>
</html>
```

 Visitors activating this link (either by clicking it with a mouse, activating it with the keyboard, or even by voice in some cases) will leave the current page and go to the Opera home page. There are more changes happening to the link itself, and we'll look at those later when we talk about link styling.

The anchor tag has several attributes you can add:

-   `href` — the resource the link points to (either an external file or an anchor ID).
-   `id` — a unique identifier for the link, useful for styling a link with CSS or referencing it with JavaScript. You can also use an `id` attribute to make a link into a page anchor, and link to it from other `<a>` elements.
-   `class` — a CSS class name to apply to the link, useful if, for example, if you want to style certain links on the page but not others.
-   `title` — extra information about the link that the browser should display on hover.

Let's go through the most important attributes first and then talk about what you can do to links to make things easier for your visitors.

## The href attribute

An `<a>` element can play several roles, depending on which attributes are set. The most common attribute you'll use is the `href` attribute, which defines what resource the link points to. This attribute can contain different values:

-   A URL relative to the current folder, e.g., "../../help/help.html" (two dots means "go up one level in the site folder hierarchy"), or a URL absolute to the server root, e.g., "/help/help.html" (a forward slash at the beginning of the URL means the address starts at the root of the folder hierarchy the current page is on).
-   A URL on a different server, for example "ftp://ftp.opera.com/" or "http://developer.yahoo.com/yui".
-   A fragment identifier or id preceded by a hash sign, e.g., "\#menu". This points to a target inside the current document rather than an external URL.
-   A mixture of URLs and fragment identifiers. That is, you can link directly to a section of a different document by pointing the `href` attribute to a URL followed by a fragment identifier, for example "http://dev.opera.com/articles/view/new-structural-elements-in-html5/\#aside".

## Creating intra-page navigation with id attributes

You can also put an `id` attribute on an `<a>` element to make it into a page anchor. Page anchors are intra-page *targets* for other links on that page. You link to them by putting the ID in the `href` attribute of another link. For example, here's an anchor coded to be a link target:

``` {.html}
<h2><a id="sec1">Section #1</a></h2>
```

 That target could be linked to by this link:

``` {.html}
<a href="#sec1">Section One</a>
```

 Handily, most browsers today allow you to write this in "shorthand" by putting the ID directly on the element you want to link to, like this:

``` {.html}
<h2 id="sec1">Section #1</h2>
```

 This is much simpler, and we recommend that you do it this way whenever possible.

The following HTML contains examples of the different types of links:

``` {.html}
<!DOCTYPE html>

<html lang="en-GB">
<head>
  <meta charset="utf-8">
  <title>Different Links Example</title>
  <link rel="stylesheet" href="linkexamplestyles.css">
</head>
<body>
  <h1>Different Links</h1>

  <h2>Example of in-page navigation with fragment identifiers, links, and anchors</h2>
  <div id="nav">
    <ul id="toc">  <!--Table of Contents-->
      <li><a href="#sec1">Section One</a></li>
      <li><a href="#sec2">Section Two</a></li>
      <li><a href="#sec3">Section Three</a></li>
      <li><a href="#sec4">Section Four</a></li>
      <li><a href="#sec5">Section Five</a></li>
    </ul>
  </div>

  <div id="content">
    <div>
      <h2 id="sec1">Section #1</h2>
      <p><a href="#toc">Back to menu</a></p>
    </div>
    <div>
      <h2 id="sec2">Section #2</h2>
      <p><a href="#toc">Back to menu</a></p>
    </div>
    <div>
      <h2 id="sec3">Section #3</h2>
      <p><a href="#toc">Back to menu</a></p>
    </div>
    <div>
      <h2 id="sec4">Section #4</h2>
      <p><a href="#toc">Back to menu</a></p>
    </div>
    <div>
      <h2 id="sec5">Section #5</h2>
      <p><a href="#toc">Back to menu</a></p>
    </div>
  </div>

  <h2>Some other link examples</h2>

  <ul>
    <li><a href="http://dev.opera.com">Opera Developer Network</a></p></li>
    <li><a href="http://www.wait-till-i.com/stuff/JavaScript-DOM-Cheatsheet.pdf">Dom Cheatsheet</a></p></li>
    <li><a href="ftp://get.opera.com/pub/opera/win/">Download different Opera versions</a></li>
    <li><a href="http://farm1.static.flickr.com/56/188791635_0b8bdd808d.jpg?v=0">Photo of my book</a></li>
  </ul>

  </body>
</html>
```

 Open this file in your browser of choice and experiment with it. You'll find that activating any of the links in the first list will jump to the appropriate section of the same page. You might also have realized that the URL in the location bar of your browser changed and now shows the fragment identifier at the end of it, which means visitors can bookmark this section or email the link to other people to send them exactly where they should go. To recap:

-   Anchor links can have a fragment identifier as the value of the `href` attribute. This fragment identifier must start with a hash sign (\#).
-   When activated, this link will jump to any HTML element with an `id` of this value. All IDs on a page must be unique.
-   IDs follow certain naming conventions. Most important is that they must start with an alphanumeric character and must not contain spaces.

That covers the menu and the different sections in the example, but what about the other links? If you try them out you'll see that they point to different targets — one goes to another site, another displays a photo, and the third one shows a specific section of another web page (found by jumping to a specific ID). If all of that worked for you, great — but what if your browser couldn't understand some of the resources?

## Don't leave any ambiguity about what you're linking to

An important thing to remember about links is that they are a substantial part of your relationship with your visitors. Readers trust that when you offer them a link, they can follow it and get good, relevant information. If your links don't work because the linked resource is not available or is in a format the visitor's browser cannot consume, you will betray that trust and lose credibility. Don't let that happen.

### Providing extra information with a title attribute

As with most other HTML elements, you can add a `title` attribute to an `<a>` element to include some extra information. Browsers will show a *tooltip* when visitors hover the mouse cursor over the link. The tooltip typically tells them what the link is about. For example, you could give a small introduction to the content and location of the linked document:

``` {.html}
<!DOCTYPE html>

<html lang="en-GB">
<head>
  <meta charset="utf-8">
<title>Adding extra information with a title attribute</title>
<link rel="stylesheet" href="linkexamplestyles.css">
</head>
<body>
  <h1>Adding extra information with a title attribute</h1>
  <ul>
    <li>Find more information on the <a title="The Yahoo Developer Network is the hub for Yahoo's developer tools"
     href="http://developer.yahoo.com">Yahoo Developer Network</a>.</li>
  </ul>
</body>
</html>
```

 However, you cannot expect visitors to have enough patience and hand-eye coordination to rely on this for crucial information. Visually impaired users, who cannot see the page well (or perhaps at all), are very likely not to be able to reach this information. While screen readers have the option to read out `title` attributes for the end user, this feature is generally turned off by default. This is why you should never use the `title` attribute for crucial information about the link.

Crucial information might be:

-   Linking to non-HTML resources like PDF files, images, videos, sound files, or downloads.
-   Leaving the current site and linking to another server (external links).
-   Linking to a document that will open in a different frame or a popup.

### Linking to non-HTML resources — don't make people guess

It can be very annoying when you click a link and your browser does not know what to do with the content the link points to. It is unfortunately all too common to see websites link to images, PDF documents, and videos without telling their visitors what to expect. Further, the resource might be quite large, which means that visitors might prefer to download it rather than opening it inside the browser, or they might prefer to not access it at all.

One of the biggest success factors for a web page is not making users guess what will happen when they perform an action. Instead, tell them directly what effects the action will have. In the case of linked resources, all you need to do is tell your visitors what the linked resource is. Here are some examples:

``` {.html}
<!DOCTYPE html>

<html lang="en-GB">
<head>
  <meta charset="utf-8">
<title>Linking non-HTML resources</title>
<link rel="stylesheet" href="linkexamplestyles.css">
</head>
<body>
  <h1>Linking non-HTML resources</h1>

  <ul>
    <li>Find more information on the <a href="http://developer.yahoo.com">Yahoo
      Developer Network site (external)</a></li>
    <li>Download the <a href="http://www.wait-till-i.com/stuff/JavaScript-DOM-Cheatsheet.pdf">
      Dom Cheatsheet (PDF, 85KB)</a></li>
    <li>Pick and <a href="ftp://get.opera.com/pub/opera/win/">download different Opera
      versions from their FTP (external)</a></li>
    <li>Check out a <a href="http://farm1.static.flickr.com/56/188791635_0b8bdd808d.jpg?v=0">
      Photo of my book (JPG, 200KB)</a></li>
  </ul>

</body>
</html>
```

 By providing information about linked files and their nature, you leave the decision of what to do with them to your visitors, rather than expecting them to have certain browser settings or pre-installed software. If you mix that information with clever styling you can even make such links look attractive and intuitive, for example, by giving different types of links easily recognisable icons (see more about this in [guides/Styling lists and links](/guides/Styling_lists_and_links)). If you want to be very safe, you can also offer a help section that explains what the different file formats are and where you can get the software needed to display them.

## External vs. internal links

One of the biggest fears for business websites is people leaving the site prematurely. This is often the reason for sites not offering third-party links (unless the third parties pay money for the privilege of having web traffic directed to them). We'll come back to this error in judgment later; for now let's talk about what developers can do to help prevent visitors from inadvertantly leaving their sites and how these measures affect the site's success.

### Frames and popups — just say no

The fear of losing visitors to other sites while still wanting to link to them gave us two innovations(?) in web development that have been a thorn in usability's side for years: frames and popups.

Using HTML frames means you separate the page shown in the browser into several different documents. The benefit is that the document seemingly stays the same even when you load different content, either from your own server or from third party servers. This is where the usefulness ends, however. Simply put, frames provide a terrible user experience. For example, when a site uses frames:

-   Search engines cannot index the whole page. In search results, they might instead show only parts of a page that don't make sense out of context.
-   Visitors cannot bookmark the page in the condition they view it. The next time they open that bookmark they'll see the initial state of the frameset, not the page as they left it.
-   Visitors who are dependent on assistive technology have a very hard time navigating around framesets.
-   Third parties might not want their sites to be shown inside a frameset and thus use "framebreaker" scripts that replace framesets with the real URL when you try to embed them. This is also used to stop criminals luring Internet users into entering personal information into a

legitimate-looking website ("phishing").

Links inside a frameset use the `target` attribute of the anchor to target the correct frame. Each frame in a frameset gets a unique name and activating the link opens the document defined in the `href` attribute in that frame. If the frameset is not available (for example, if a visitor found the document with the links via a search engine), each link opens in a new browser instance.

Opening a new browser instance is another common way to link to third party sites, either with a scripted pop-up window or with a `target` attribute with a value of `_blank`. The fact that every modern browser comes with a pop-up blocker should give an indication of how unpopular this technique is today!

In short, **do not use the `target` attribute when you create links unless you know what you are doing**. It is an outdated idea anyway; today, virtually all browsers have tabbed interfaces, so users can easily open third-party sites in a different tab without leaving your site. Under certain circumstances you may want to indicate the difference between external and internal links, but always leave it to the discretion of the visitor what to do with them.

### Benefits of outbound and inbound links

There are several good reasons for linking to third party sites even when they are competitors.

-   It gives you credibility in the eyes of your visitors, telling them you are so sure of the quality of your content that you don't avoid competition.
-   It is an opportunity to deliver a full service. You can link to content and articles or even products on other sites that you don't cover but that might be of interest for those visitors who want to dive deeper into the topic at hand.
-   You can prove a point by building on an older article by a third party and offering a better or different solution while referencing the old article via a link.

The usefulness of inbound links (links pointing from a third-party site to yours) is less debated. The more often that other, high-quality sites link to yours, the higher you'll rank in search engines. Before that happens, however, you need to prove that you don't shy away from linking to others either.

This brings us to another very important part of creating good links: how to word them.

## Link wording

We covered this briefly in the section about linking to non-HTML resources, but it is good to remind ourselves that links are not just interactive elements, but also an integral part of the page copy.

Some assistive technologies will offer a list of links instead of the whole document to allow visitors to quickly navigate it and find the link they want. This means that your link text needs to make sense out of context as well as in context. You can easily check this in Opera by opening any website and choosing `Tools > Links` from the menu or pressing `Ctrl + Shift + L`. You'll get a new tab that shows all the links in the document and the resources they point to.

You should also make sure that your page doesn't contain multiple links with the same wording but pointing to different resources. The classic mistake is "click here" links, worded like "To download the latest version of our tool <u>click here</u>". It's much better to use link text that explains what the link points to. For example, turn that sentence into "You can <u>download the latest version of our tool</u> and try it out for yourself."

The same applies to "more" links. These are often found in news sites, where you see a heading and some teaser text followed by a "more" or "full story" link. The solution to this problem is to either use a linked "more" image with some unique alternative text, or to add a `<span>` element inside the link after the "more" and hide it with CSS.

## Link styling

A full treatment of link styling is beyond the scope of this article (but you can find more information in [guides/Styling lists and links](/guides/Styling_lists_and_links)). Still, it is important to remember that how links look is very important and that there are several different link states to consider. The link states (called CSS *pseudo class selectors*) are:

-   `:link` (default) — defines the style of unvisited links in general. By default, unvisited links are blue.
-   `:visited` — defines the style of links that have already been clicked (visited). By default, already visited links are purple.
-   `:hover` — defines the style of a link while the mouse cursor is hovering over it.
-   `:focus` — defines the style of a link when it has focus (or highlighted) by a mouse click or via another alternative control mechanism such as the keyboard.
-   `:active` — defines the style of the link while it is activated; that is, while the connection to its target is in progress. This is also the style of the last activated link when you arrive at a document by using the browser's Back function.

## HTML5: block level linking

In HTML4, the `<a>` element was restricted to turning other inline elements into links. This was fine for most situations, but it became annoying when you wanted, for example, to turn an entire advertising banner section containing images and paragraphs into a link. For the code to remain valid, you would have to wrap each individual bit of text and each image in its own separate link — all going to the same place — which is not only horribly repetitious, but confuses assistive technology and its users. Putting an inline element around a section of block level content also makes styling behave weirdly, unless you remember to set it to display like a block level element using CSS.

Fortunately, HTML5 removes this restriction, allowing you to put a single link around any amount of content you want. To get it to behave properly, you still have to set the link to behave like a block level element, but this is easy, and far more flexible than it used to be. Let's look at an example:

``` {.html}
<!DOCTYPE html>

<html lang="en-GB">
<head>
  <meta charset="utf-8">
  <title>Block level link Example</title>
  <link rel="stylesheet" href="styles.css">
  <style>
    a {
      display: block;
      background-color: blue;
      text-decoration: none;
      color: white;
      width: 300px;
      height: 100px;
    }

    a:hover {
      background-color: red;
    }

  </style>
</head>
<body>
  <a href="http://www.opera.com">
    <h1>A link to Opera</h1>
    <p>Opera Software</p>
  </a>
</body>
</html>
```

 Here you can see that we have the `<a>` element wrapping both a heading and a paragraph. To make this work correctly we've set it to `display: block;` in the CSS. If you try the example out yourself, you'll see that the entire block is part of the clickable link area. I have also added a background-color change on hover to make this more visible.

## Conclusion

We covered a lot in this article, but perhaps the most important takeaway is to remember not only what links do, but what they **should** do.

## See also

### Exercise questions

-   What is wrong with the following link: `<a href="report.pdf" title="report as PDF, 2.3MB">get our latest report</a>`?
-   What is the `target` attribute in links for and are there any good uses for it?
-   I’ve talked about link relationships and connections between links and anchors. Is there an attribute for links that describes relationships between documents, too?
-   How can you write a link that sends the visitors to an element further down the page when they click it? What do you need to make sure of beforehand?

