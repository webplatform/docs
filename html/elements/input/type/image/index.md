---
title: image
tags:
  - Pages
  - using
  - duplicate
  - arguments
  - in
  - template
  - calls
  - Markup
  - Elements
  - HTML
readiness: 'Not Ready'
notes:
  - 'Merge Candidate: html/attributes/type. Add example.'
summary: 'The image type of the <input> element represents an image. The user can either use the image as a button to submit the form, or select a coordinate of the image to be submitted with the form data.'
uri: html/elements/input/type/image

---
# image

## Summary

The image type of the \<input\> element represents an image. The user can either use the image as a button to submit the form, or select a coordinate of the image to be submitted with the form data.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLInputElement](/dom/HTMLInputElement)

**Needs Examples**: This section should include examples.

## Notes

### Remarks

The x-coordinate is submitted under the name of the control with `.x` appended, and the y-coordinate is submitted under the name of the control with `.y` appended. Any [**value**](/html/attributes/value_(li_element)) property is ignored. The [**src**](/html/attributes/src_(iframe,_embed,_xml)) property specifies the **img** element. The following image and video file formats are supported:

-   .avi—Audio-Visual Interleaved (AVI)
-   .bmp—Windows Bitmap (BMP)
-   .emf—Windows Enhanced Metafile (EMF)
-   .png—Graphics Interchange Format (GIF)
-   .png, .jpeg—Joint Photographic Experts Group (JPEG)
-   .mov—Apple QuickTime Movie (MOV)
-   .mpg, .mpeg—Motion Picture Experts Group (MPEG)
-   .png—Portable Network Graphics (PNG)
-   .wmf—Windows Metafile (WMF)
-   .xbm—X Bitmap (XBM)

In IE8 Standards mode or later, the [**title**](/html/attributes/title) attribute is preferred over the [**alt**](/html/attributes/alt) attribute when specified as a pop-up tooltip. In addition, the value of the [**src**](/html/attributes/src_(iframe,_embed,_xml)) attribute depends on the current document compatibility mode.

### Standards information

-   [HTML 4.01 Specification](http://go.microsoft.com/fwlink/p/?linkid=25320), Section 17.4
-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374), Section 4.10.7.1.20

### HTML information

{

## See also

### Related pages (MSDN)

-   `Reference`
-   `img`
-   `input`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

