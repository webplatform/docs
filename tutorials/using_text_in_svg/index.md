---
title: Using text in SVG
attributions:
  - 'This article contains content originally from external sources, including ones licensed under the CC-BY-SA license. [![cc-by-sa-small-wpd.png](/assets/public/c/c8/cc-by-sa-small-wpd.png)](http://creativecommons.org/licenses/by-sa/3.0/us/)'
  - 'Portions of this content copyright 2012 Mozilla Contributors. This article contains work licensed under the Creative Commons Attribution-Sharealike License v2.5 or later. The original work is available at Mozilla Developer Network: [Article](https://developer.mozilla.org/en-US/docs/SVG/Tutorial/Texts)'
readiness: 'Ready to Use'
summary: 'This article details how to insert text into an SVG image.'
tags:
  - Tutorials
  - SVG
uri: 'tutorials/using text in svg'

---
## Summary

This article details how to insert text into an SVG image.

When talking about text in SVG we have to differentiate two almost completely separate topics. The one is the inclusion and display of text in an image, and the other are SVG fonts. The later may be described in a later section of the tutorial, while we will focus completely on the first part: Bringing text into an SVG image.

### Basics

We can see in this example that the `text` element can be used to put arbitrary text in SVG documents:

    <text x="10" y="10">Hello World!</text>

The `x` and `y` attributes determine, where in the viewport the text will appear. The attribute `text-anchor`, which can have the values start, middle, end or inherit, allows to decide, in which direction the text flows from this point.

Like with the shape elements text can be colorized with the `fill` attribute and given a stroke with the `stroke` attribute. Both may also refer to gradients or patterns, which makes simple coloring text in SVG very powerful compared to CSS 2.1.

### Setting font properties

An essential part of a text is the font in which it is displayed. SVG offers a set of attributes, many similar to their CSS counterparts, to enable font selection. Each of the following properties can be set as an attribute or via a CSS declaration: `font-family`, `font-style`, `font-weight`, `font-variant`, `font-stretch`, `font-size`, `font-size-adjust`, `kerning`, `letter-spacing`, `word-spacing` and `text-decoration`.

### Other text-related elements

#### tspan

This element is used to mark up sub-portions of a larger text. It must be a child of a `text` element or another `tspan` element. A typical usecase is to paint one word of a sentence bold red.

    <text>
      <tspan font-weight="bold" fill="red">This is bold and red</tspan>
    </text>

The tspan element has the following custom attributes:

**x**
 Set a new absolute x coordinate for the containing text. This overwrites the default current text position. The attribute may also contain a list of numbers, that are one by one applied to the single characters of the tspan element.

**dx**
 Start drawing the text with a horizontal offset dx from the default current position. Here, too, you may provide a list of values that are applied to consecutive characters, hence piling up the offset over time.

Likewise there are **y** and **dy** for vertical displacement.

**rotate**
 Rotate all charactes by this degree. A list of numbers makes each character rotate to its respective value, with remaining characters rotating according to the last value.

**textLength**
 This is a more obscure attribute giving the calculated length of the string. It is meant to allow the rendering engine to fine-tune the positions of the glyphs. when its own measured text length doesn't meet the one provided here.

##### tref

The `tref` element allows to reference already defined text, effectively copying it in its place. You can use the `xlink:href` attribute to point it to an element who's text content is to be taken over. You can then style it and modify it's appearance independent of the source.

    <text id="example">This is an example text.</text>

    <text>
        <tref xlink:href="#example" />
    </text>

##### textPath

This element fetches via its `xlink:href` attribute an arbitrary path and aligns the characters, that it encircles, along this path:

    <path id="my_path" d="M 20,20 C 40,40 80,40 100,20" />
    <text>
      <textPath xlink:href="#my_path">This text follows a curve.</textPath>
    </text>
