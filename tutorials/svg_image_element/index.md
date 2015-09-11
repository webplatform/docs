---
title: SVG image element
attributions:
  - 'This article contains content originally from external sources, including ones licensed under the CC-BY-SA license. [![cc-by-sa-small-wpd.png](/assets/public/c/c8/cc-by-sa-small-wpd.png)](http://creativecommons.org/licenses/by-sa/3.0/us/)'
  - 'Portions of this content copyright 2012 Mozilla Contributors. This article contains work licensed under the Creative Commons Attribution-Sharealike License v2.5 or later. The original work is available at Mozilla Developer Network: [Article](https://developer.mozilla.org/en-US/docs/SVG/Tutorial/SVG_Image_Tag)'
notes:
  - 'Fix broken link'
readiness: 'Almost Ready'
summary: 'This article describes the usage of the SVG image element'
tags:
  - Tutorials
  - SVG
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - 'W3 specs'
uri: 'tutorials/svg image element'

---
## <span>Summary</span>

This article describes the usage of the SVG image element

The SVG image element allows for raster images to be rendered within an SVG object.

In this basic example, a .jpg image will be rendered inside an SVG object:

    <?xml version="1.0" standalone="no"?>
    <!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 1.1//EN"
      "http://www.w3.org/Graphics/SVG/1.1/DTD/svg11.dtd">
    <svg width="5cm" height="4cm" version="1.1"
         xmlns="http://www.w3.org/2000/svg" xmlns:xlink= "http://www.w3.org/1999/xlink">
        <image xlink:href="firefox.jpg" x="0" y="0" height="50px" width="50px"/>
    </svg>

There are some important things to take note of (referenced from the [W3 specs](/w/index.php?title=W3_specs&action=edit&redlink=1))

-   If you do not set the x or y attributes, they will be set to 0
-   If you do not set the height or width attributes, they will be set to 0
-   Having a height or width attribute of 0 will disable rendering of the image
