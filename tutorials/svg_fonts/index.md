---
title: svg fonts
tags:
  - Tutorials
  - SVG
readiness: 'In Progress'
notes:
  - 'Fix multiple broken links'
summary: 'This article covers the creation and usage of SVG fonts.'
uri: 'tutorials/svg fonts'
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - 'postponed implementation indefinitely'
    - WOFF
    - 'Adobe SVG Viewer'
    - 'from the specification'
    - '@font-face'
    - ascenders
    - 'Template:SVGElement("font")'
    - 'Template:SVGElement("font-face")'
    - 'Template:SVGElement("font-face-src")'
    - 'Template:SVGElement("font-face-name")'
    - 'Template:SVGElement("font-face-uri")'
    - 'Template:SVGElement("missing-glyph")'
    - 'Template:SVGElement("filter")'
    - 'Template:SVGElement("a")'
    - 'Template:SVGElement("script")'
    - 'Template:SVGElement("glyph")'
    - 'Template:SVGElement("hkern")'
    - 'Template:SVGElement("vkern")'

---
# SVG fonts

## Summary

This article covers the creation and usage of SVG fonts.

When SVG was specified support for web fonts was far from being expected. Since the correct font is however crucial for the rendering of a graphic, it was decided to add a font description technology to SVG. It was not meant to concur with other formats like PostScript or OTF, but as a simple means of embedding glyph information for rendering engines.

SVG Fonts browser support covers all modern browsers (desktop and mobile) except Firefox and Internet Explorer. Firefox has [postponed implementation indefinitely](/w/index.php?title=postponed_implementation_indefinitely&action=edit&redlink=1) to concentrate on [WOFF](/w/index.php?title=WOFF&action=edit&redlink=1). However, other tools, like the [Adobe SVG Viewer](/w/index.php?title=Adobe_SVG_Viewer&action=edit&redlink=1) plugin, Batik and in parts Inkscape support them.

The base for defining an SVG font is the [Template:SVGElement("font")](/w/index.php?title=Template:SVGElement(%22font%22)&action=edit&redlink=1) element.

## Defining a font

There are some elements involved in getting all information together, that is needed for a font. I will first show an example declaration (the one [from the specification](/w/index.php?title=from_the_specification&action=edit&redlink=1)) and afterwards explain the details.

    <font id="Font1" horiz-adv-x="1000">
      <font-face font-family="Super Sans" font-weight="bold" font-style="normal"
          units-per-em="1000" cap-height="600" x-height="400"
          ascent="700" descent="300"
          alphabetic="0" mathematical="350" ideographic="400" hanging="500">
        <font-face-src>
          <font-face-name name="Super Sans Bold"/>
        </font-face-src>
      </font-face>
      <missing-glyph><path d="M0,0h200v200h-200z"/></missing-glyph>
      <glyph unicode="!" horiz-adv-x="300"><!-- Outline of exclam. pt. glyph --></glyph>
      <glyph unicode="@"><!-- Outline of @ glyph --></glyph>
      <!-- more glyphs -->
    </font>

We start with the [Template:SVGElement("font")](/w/index.php?title=Template:SVGElement(%22font%22)&action=edit&redlink=1) element. It bears an id attribute, that is needed if you want to reference it via URI (see below). The `horiz-adv-x` attribute determines, how wide a character is on average compared to the path definitions of the single glyphs. The value `1000` sets a reasonable value to work in. There are several accompanying attributes, that help further defining the basic glyph-box layout.

The [Template:SVGElement("font-face")](/w/index.php?title=Template:SVGElement(%22font-face%22)&action=edit&redlink=1) element is the counterpart of the CSS [@font-face](/w/index.php?title=@font-face&action=edit&redlink=1) declaration. It defines basic properties of the final font, as how to classify its weight, style and so forth. In the example above the first and most important to be defined is `font-family`. Its value can then be referenced in CSS and SVG `font-family` properties. The `font-weight` and `font-style` attributes have the same purpose. All following attributes are rendering instructions to the font layout engine, for example, how much of the glyphs' overall height are [ascenders](/w/index.php?title=ascenders&action=edit&redlink=1).

Its child, the [Template:SVGElement("font-face-src")](/w/index.php?title=Template:SVGElement(%22font-face-src%22)&action=edit&redlink=1) element, corresponds to CSS' `src` property in `@font-face` declarations. You can point to external sources for font declarations by means of its children [Template:SVGElement("font-face-name")](/w/index.php?title=Template:SVGElement(%22font-face-name%22)&action=edit&redlink=1) and [Template:SVGElement("font-face-uri")](/w/index.php?title=Template:SVGElement(%22font-face-uri%22)&action=edit&redlink=1). The example states, that if the renderer has a local font at hand named "Super Sans Bold", it should use this instead.

Following [Template:SVGElement("font-face-src")](/w/index.php?title=Template:SVGElement(%22font-face-src%22)&action=edit&redlink=1) is a [Template:SVGElement("missing-glyph")](/w/index.php?title=Template:SVGElement(%22missing-glyph%22)&action=edit&redlink=1) element. This declares, what should be displayed, if a certain glyph is not found in the font, and if there are no fallback mechanisms. It also shows, how glyphs are created: By simply adding any graphical SVG content inside. You can use literally any other SVG elements in there, even [Template:SVGElement("filter")](/w/index.php?title=Template:SVGElement(%22filter%22)&action=edit&redlink=1), [Template:SVGElement("a")](/w/index.php?title=Template:SVGElement(%22a%22)&action=edit&redlink=1) or [Template:SVGElement("script")](/w/index.php?title=Template:SVGElement(%22script%22)&action=edit&redlink=1). For simple glyphs, however, you can simply add a `d` attribute that works exactly like for paths.

The actual glyphs are then defined by [Template:SVGElement("glyph")](/w/index.php?title=Template:SVGElement(%22glyph%22)&action=edit&redlink=1) elements. The most important attribute is `unicode`. It defines the Unicode Codepoint, that is represented by this glyph. If you specify the `lang` attribute, you can furthermore restrict the glyph for certain languages (represented by `xml:lang` on the target) exclusively. Again, you can use arbitrary SVG to define the glyph, which allows for great effects in conforming user agents.

There are two further elements, that can be defined inside `font`, [Template:SVGElement("hkern")](/w/index.php?title=Template:SVGElement(%22hkern%22)&action=edit&redlink=1) and [Template:SVGElement("vkern")](/w/index.php?title=Template:SVGElement(%22vkern%22)&action=edit&redlink=1). Each instance carries references to at least two characters and an attribute k that determines how much the distance between those characters should be decreased. The basic example are "A" and "V", where renderers should place "AV" much narrower than the single character definitions imply.

    <hkern u1="A" u2="V" k="20" />

## Referencing a font

This is a fairly simple one. If you have put together your font declaration as described above, you can just use a simple `font-family` attribute.

    <font>
      <font-face font-family="Super Sans" />
      <!-- and so on -->
    </font>

    <text font-family="Super Sans">My text uses Super Sans</text>

However, you are free to combine several methods for great freedom of how and where to define the font.

### Option: Use CSS @font-face

You can use @font-face to reference remote (and not so remote) fonts.

    <font id="Super_Sans">
      <!-- and so on -->
    </font>

    <style type="text/css">
    @font-face {
      font-family: "Super Sans";
      src: url(#Super_Sans);
    }
    </style>

    <text font-family="Super Sans">My text uses Super Sans</text>

### Option: reference a remote font

The above mentioned font-face-uri allows to reference an external font, hence allowing greater re-usability.

    <font>
      <font-face font-family="Super Sans">
        <font-face-src>
          <font-face-uri xlink:href="fonts.svg#Super_Sans" />
        </font-face-src>
      </font-face>
    </font>

## Attribution

*This article contains content originally from external sources, including ones licensed under the CC-BY-SA license.* [![cc-by-sa-small-wpd.png](/assets/public/c/c8/cc-by-sa-small-wpd.png)](http://creativecommons.org/licenses/by-sa/3.0/us/)

Portions of this content copyright 2012 Mozilla Contributors. This article contains work licensed under the Creative Commons Attribution-Sharealike License v2.5 or later. The original work is available at Mozilla Developer Network: [Article](https://developer.mozilla.org/en-US/docs/SVG/Tutorial/SVG_fonts)

