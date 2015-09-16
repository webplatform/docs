---
title: SVG clipping and masking
attributions:
  - 'This article contains content originally from external sources, including ones licensed under the CC-BY-SA license. [![cc-by-sa-small-wpd.png](/assets/public/c/c8/cc-by-sa-small-wpd.png)](http://creativecommons.org/licenses/by-sa/3.0/us/)'
  - 'Portions of this content copyright 2012 Mozilla Contributors. This article contains work licensed under the Creative Commons Attribution-Sharealike License v2.5 or later. The original work is available at Mozilla Developer Network: [Article](https://developer.mozilla.org/en-US/docs/SVG/Tutorial/Clipping_and_masking)'
notes:
  - 'Fix broken link'
readiness: 'Almost Ready'
summary: 'This article explains how clipping and masking work in SVG.'
tags:
  - Tutorials
  - SVG
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - 'Template:SVGElement("clipPath")'
uri: 'tutorials/svg clipping and masking'

---
## Summary

This article explains how clipping and masking work in SVG.

Erasing part of what one has created cumbersome might at first sight look contradictory. But when you try to create a semicircle in SVG, you will find out the use of the following properties quickly.

**Clipping** refers to removing parts of elements defined by other parts. In this case, any half-transparent effects are not possible; it's an all-or-nothing approach.

**Masking** on the other hand allows soft edges by taking transparency and grey values of the mask into account.

### Creating clips

We create the above mentioned semicircle based on a `circle` element:

    <clipPath id="cut-off-bottom">
      <rect x="0" y="0" width="200" height="100" />
    </clipPath>

    <circle cx="100" cy="100" r="100" clip-path="url(#cut-off-bottom)" />

Centered at (100,100), a circle with radius 100 is painted. The attribute `clip-path` references a `Template:SVGElement("clipPath")` element with a single `rect` element. This rectangular on its own would paint the upper half of the canvas black. Note that the `clipPath` element is usually placed in a `defs` section.

The `rect` will not be painted, however. Instead, its pixel data will be used to determine which pixels of the circle "make it" to the final rendering. Since the rectangle covers only the upper half of the circle, the lower half of the circle will vanish:

![clipdemo.png](/assets/public/1/1a/clipdemo.png)

We now have a semicircle without having to deal with arcs in path elements. For the clipping, every path inside the `clipPath` is inspected and evaluated together with its stroke properties and transformation. Then every part of the target lying in a transparent area of the resulting `clipPath`'s content will not rendered. Color, opacity and such have no effect as long as they don't let parts vanish completely.

### Masking

The effect of masking is most impressively presented with a gradient. If you want an element to fade out, you can achieve this effect quite quickly with masks.

    <svg version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink">
      <defs>
        <linearGradient id="Gradient">
          <stop offset="0" stop-color="white" stop-opacity="0" />
          <stop offset="1" stop-color="white" stop-opacity="1" />
        </linearGradient>
        <mask id="Mask">
          <rect x="0" y="0" width="200" height="200" fill="url(#Gradient)"  />
        </mask>
      </defs>

      <rect x="0" y="0" width="200" height="200" fill="green" />
      <rect x="0" y="0" width="200" height="200" fill="red" mask="url(#Mask)" />
    </svg>

You see a green-filled `rect` at the lowest layer and on top a red-filled `rect`. The latter has the `mask` attribute pointing to the `mask` element. The content of the mask is a single `rect` element, that is filled with a transparent-to-white gradient. As a result the pixels of the red rectangle inherit the alpha value (the transparency) of the mask content, and we see a green-to-left gradient as a result:

![maskdemo.png](/assets/public/e/ec/maskdemo.png)

### Transparency with opacity

There is a simple possibility to set the transparency for a whole element. It's the `opacity` attribute:

    <rect x="0" y="0" width="100" height="100" opacity=".5" />

The above rectangle will be painted half-transparent. For the fill and stroke, there are two separate attributes, `fill-opacity` and `stroke-opacity`, that control each of those property opacities separately. Note that the stroke will be painted on top of the filling. Hence, if you set a stroke opacity on an element that also has a fill, the fill will shine through on half of the stroke, while on the other half the background will appear:

    <rect x="0" y="0" width="200" height="200" fill="blue" />
    <circle cx="100" cy="100" r="50" stroke="yellow" stroke-width="40" stroke-opacity=".5" fill="red" />

![opacitydemo.png](/assets/public/3/3e/opacitydemo.png)

You see in this example the red circle on blue background. The yellow stroke is set to 50% opacity, which effectively leads to a double-color stroke.

## Using well-known CSS techniques

One of the most powerful tools in a web developer's toolbox is `display: none`. There is therefore little surprise that it was decided to take this CSS property into SVG as well, together with `visibility` and `clip` as defined by CSS 2. For reverting a previously set `display: none`, it is important to know that the initial value for all SVG elements is `inline`.
