---
title: 'SVG links'
notes:
  - 'Fix a couple of broken links'
readiness: 'Almost Ready'
summary: 'This tutorial covers the creation of links inside SVG objects.'
tags:
  - Tutorials
  - SVG
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - 'HTML links – let’s build a web!'
    - 'SVG specification'
uri: 'tutorials/svg links'

---
## Summary

This tutorial covers the creation of links inside SVG objects.

## Introduction

Just like (X)HTML, SVG supports linking to content within the document and to external resources, for example other SVG documents, HTML or XML documents, images, videos or any other kind of typical resource you may want to link to. This tutorial will walk you through how to create links in SVG using Xlink—the W3C spec for linking in XML—and cover any specific SVG-related concerns that you man need to know.

If you are not familiar with the `a` element or the `href` attribute in HTML I recommend reading Christian Heilmann’s [HTML links – let’s build a web!](/w/index.php?title=HTML_links_%E2%80%93_let%E2%80%99s_build_a_web!&action=edit&redlink=1) article before we start. It is also recommended that you read my article to familiarise yourself with the basics of SVG, if you are not already familiar.

Note: XML doesn’t support linking by default, so the situation is slightly more complex than [HTML links](/guides/html_links). But don't despair - Xlink is still not that complicated to get the hang of; after reading this article it should present you with no trouble.

## Getting started with SVG links

In HTML I can simply set up a link from one document to another using an `a` element and an `href` attribute like so:

``` html
<a href="http://example.com/link/">An example link</a>
```

 The `a` element is contained in the linking document (the local resource), and the `href` attribute points to the document or resource I want to link to (the remote resource). All very straight forward.

In XML and therefore SVG, there is no magic `href` attribute that can create links. Instead you have to use a technology called XLink to provide this functionality. XLink is a very powerful technology that provides a lot of complex functionality, such as one-to-many links, but for SVG we only have to care about simple one-to-one links, as that is all that is supported in the [SVG specification](/w/index.php?title=SVG_specification&action=edit&redlink=1).

### Setting up the XLink namespace

You've already met XML namespaces when defining a SVG template. Usually an SVG document uses the default namespace like so:

``` xml
<svg xmlns="http://www.w3.org/2000/svg" version="1.1">
  …content goes here…
</svg>
```

 Since the default namespace is taken up by SVG, if you want to to define the XLink namespace on the SVG element you have to give it a prefix, which by general convention is `xlink` (although it can be anything you please). Lets add the XLink namespace to our `svg` element:

``` xml
<svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" version="1.1">
  …content goes here…
</svg>
```

 As you can see, the `xlink` prefix is defined using the `xmlns` attribute, a colon (:) and the desired prefix. The value is then set to the standard XLink namespace.

Now the XLink namespace is set up, any time you want to refer to a XLink element or attribute on the `svg` element or any of its children, you have to use it in combination with the `xlink` prefix. The best way to explain this is with an example, so lets start to set up a similar link to the HTML link above.

### A simple SVG link using XLink

Next we need to use the SVG `a` element in our document to define a link, and the `text` element to define the link text:

``` xml
<svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" version="1.1">
  <a>
    <text x="10" y="25">An example link.</text>
  </a>
</svg>
```

 Now we have to add the XLink `href` attribute to the `a` element to specify the destination of the link, like so:

``` xml
<svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" version="1.1">
  <a xlink:href="http://example.com/link/">
    <text x="10" y="25" >An example link.</text>
  </a>
</svg>
```

 The `xlink` namespace is added before the attribute name, using a colon to separate the prefix from the attribute.

Note: It is possible to define the type of link you are using as a simple link using `xlink:type="simple"` on the `a` element, but this is optional and simple links are the only type of XLink links that are valid in SVG anyway.

Using the `a` element in SVG doesn't automatically style the link like it does in HTML, so you may want to add some styling to the text, as seen in the completed .

One thing worth remembering is that to set the colour of the text in SVG you must use the `fill` CSS property or XML attribute, not `color` as in HTML. The text must also be contained in a `text` element nested inside the link, unlike HTML where a `a` element can contain text immediately between its start and end tags.

## Adding additional functionality to links

You may recall that HTML links can have a `title` attribute to describe additional details about the link. This is also available with XLink in SVG:

``` xml
<a xlink:href="http://example.com/link/" xlink:title="The link leads to an example page that is of little interest">
  <text x="10" y="25" >An example link.</text>
</a>
```

 If you try out my example, you will see that a tooltip will show up when you hover over the link.

Following a link defaults to opening the linked resource in the same window or tab. You can change this behaviour by using the XLink `show` attribute. Using a value of `replace` specifies the default behaviour, while changing it to `new` will open the link in a new window or tab.

``` xml
<a xlink:href="http://example.com/link/" xlink:title="The link opens an example page in a new tab/window" xlink:show="new">
  <text x="10" y="25" >An example link.</text>
</a>
```

### Linking to a specific point in a document

Also like HTML, it is possible to link to a specific point in a document (both in local and remote documents) by specifying an `id` on the element you want to link to and adding a fragment identifier to the link. This can be achieved in almost exactly the same way as with HTML:

``` xml
<svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" version="1.1">
  <a xlink:href="http://www.someurl.com#someid">
    <text x="10" y="25" >An example link.</text>
  </a>
</svg>
```

 You can also link to a specific part of a SVG document, using the fragment identifier combined with the `view` element. This can be useful for defining an area of the SVG file that you'd like to zoom in or out of when the user clicks on a link or a button.

The fragment identifier works in exactly the same way as the example above, while the `view` element is used to specify the size of the viewport after the URL has been followed. I will show this with another example:

``` xml
<svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" version="1.1" width="100%" height="100%">
  <a xlink:href="#target">
    <text x="10" y="25">Zoom in on shape below</text>
  </a>

  <view id="target" viewBox="600 600 50 50"/>
  <rect x="600" y="600" width="50" height="50"/>
</svg>
```

 The `view` element requires at least two attributes, the `id` so that the fragment identifier can point to it, and the `viewBox`. The `viewBox` attribute sets the size of the viewport with four values, Minimum x co-ordinate, Minimum y co-ordinate, width and height. When the link is followed, the browser will set the viewport to the co-ordinates and width and height specified on the corresponding view element. Behind the scenes, the browser automatically applies transitions and scaling for you to make the content fit correctly in the `viewBox`.

With the example above, you may notice that the rectangle doesn’t fill your browser window. This is because by default it preserves the aspect ratio of the elements. There is a way to define this behaviour using the `preserveAspectRatio` attribute. I will cover this in a later article, but if you just want ignore the aspect ratio, you can set the value to `none` like so:

``` xml
<view id="target" viewBox="600 600 50 50" preserveAspectRatio="none"/>
```

### Embedding external resources in an SVG document

As well as linking to separate documents, it is possible to embed resources such as images into an SVG document in a very similar manner, again using the XLink href attribute. Images can either be raster images such as PNGs and JPEGS, or another SVG file:

``` xml
<svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" version="1.1">
  <image xlink:href="circle.png" x="10" y="25" height="100" width="100">
    <desc>A perfect circle</desc>
  </image>
</svg>
```

 The `desc` element provides a means to provide alternative text, in the same way that the HTML `alt` attribute does. This will be useful once screen readers begin to support SVG.

Try out my example.

Embedding an SVG image works in exactly the same way:

``` xml
<image xlink:href="circle.svg" x="10" y="25" height="100" width="100">
  <desc>A perfect circle</desc>
</image>
```

 Note: The Xlink `show` attribute is used with a value of `embed` to include resources in the document, but as this is the default (and only) value allowed for the `show` attribute on the `image` element, it can be omitted.

Fragments of SVG can be embedded in the document using the `use` element - this includes SVG from external SVG files, and fragments that have already appeared in the same document. This allows SVG elements to be defined once and reused many times, and will be the subject of an additional article on reusable SVG, to be published in the future on dev.opera.com.

SVG Tiny 1.2 and above allow for embedding of audio and video, but this is not widely implemented. At the time of writing this only works in a .

### Linking multiple elements

In HTML 4.01 and XHTML 1.0/1.1, the `a` element is inline and thus can not legally contain block level child elements. If you want to for example make an image and adjacent text into the same link, you have to specify additional `a` elements with the same `href` value. There is no such restriction with SVG - it is perfectly valid to do the following:

``` xml
<svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" version="1.1">
  <defs>
    <linearGradient id="badgeGradient">
      <stop offset="0"/>
      <stop offset="1"/>
    </linearGradient>
  </defs>

  <g id="heading">
    <a xlink:href= "http://www.opera.com/">
      <path id="badge" d="M 29.6,22.8 C 29.2,23.4 24.3,22.4 23.8,22.9 C 23.4,23.3 24.3,28.3 23.8,28.6 C 23.2,28.9 19.4,25.6 18.8,25.8 C 18.2,26.0 16.5,30.7 15.8,30.7 C 15.2,30.7 13.5,26.0 12.9,25.8 C 12.3,25.6 8.5,28.9 7.9,28.6 C 7.4,28.3 8.3,23.3 7.9,22.9 C 7.4,22.4 2.4,23.4 2.1,22.8 C 1.8,22.3 5.1,18.4 4.9,17.8 C 4.8,17.2 0.0,15.5 0.0,14.9 C 0.0,14.3 4.8,12.6 4.9,12.0 C 5.1,11.4 1.8,7.5 2.1,7.0 C 2.4,6.4 7.4,7.3 7.9,6.9 C 8.3,6.5 7.4,1.5 7.9,1.2 C 8.5,0.9 12.3,4.1 12.9,4.0 C 13.5,3.8 15.2,-0.8 15.8,-0.8 C 16.5,-0.8 18.2,3.8 18.8,4.0 C 19.4,4.1 23.2,0.9 23.8,1.2 C 24.3,1.5 23.4,6.5 23.8,6.9 C 24.3,7.3 29.2,6.4 29.6,7.0 C 29.9,7.5 26.6,11.4 26.8,12.0 C 26.9,12.6 31.7,14.3 31.7,14.9 C 31.7,15.5 26.9,17.2 26.8,17.8 C 26.6,18.4 29.9,22.3 29.6,22.8 z"/>
      <text id="label" x="5" y="20" transform = "rotate(-15 10 10)">New</text>
      <text id="title" x="40" y="20">Opera Browser</text>
    </a>
  </g>

</svg>
```

 Try it out by viewing my example.
