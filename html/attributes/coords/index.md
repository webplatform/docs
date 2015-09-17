---
title: 'coords'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: coords
  topic: html
notes:
  - 'Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info'
readiness: 'Not Ready'
tags:
  - Markup_Attributes
  - HTML
  - Needs_Summary
uri: html/attributes/coords

---
<table class="wikitable">
<tr>
<th>
Applies to

</th>
<td>
 ?

</td>
</tr>
</table>
## Examples

This example provides the full code for an image map of the solar system. Clicking on the sun or any planet links to an individual image.

``` html
<P><IMG SRC="solarsys.png" WIDTH=504 HEIGHT=126 BORDER=0
    ALT="Solar System" USEMAP="#SystemMap">

<MAP NAME="SystemMap">
    <AREA SHAPE="rect" COORDS="0,0,82,126"
        HREF="/workshop/graphics/sun.png">
    <AREA SHAPE="circle" COORDS="90,58,3"
        HREF="/workshop/graphics/merglobe.png">
    <AREA SHAPE="circle" COORDS="124,58,8"
        HREF="/workshop/graphics/venglobe.png">
    <AREA SHAPE="circle" COORDS="162,58,10"
        HREF="/workshop/graphics/earglobe.png">
    <AREA SHAPE="circle" COORDS="203,58,8"
        HREF="/workshop/graphics/marglobe.png">
    <AREA SHAPE="poly"
        COORDS="221,34,238,37,257,32,278,44,284,60,281,75,
            288,91,267,87,253,89,237,81,229,64,228,54"
        HREF="/workshop/graphics/jupglobe.png">
    <AREA SHAPE="poly"
        COORDS="288,19,316,39,330,37,348,47,351,66,349,74,
            367,105,337,85,324,85,307,77,303,60,307,50"
        HREF="/workshop/graphics/satglobe.png">
    <AREA SHAPE="poly"
        COORDS="405,39,408,50,411,57,410,71,404,78,393,80,
            383,86,381,75,376,69,376,56,380,48,393,44"
        HREF="/workshop/graphics/uraglobe.png">
    <AREA SHAPE="poly"
        COORDS="445,38,434,49,431,53,427,62,430,72,435,77,
            445,92,456,77,463,72,463,62,462,53,455,47"
        HREF="/workshop/graphics/nepglobe.png">
    <AREA SHAPE="circle" COORDS="479,66,3"
        HREF="/workshop/graphics/pluglobe.png">
</MAP>
```

## Notes

### Remarks

For [**a**](/html/elements/a) objects, you must set the value of this property before you can retrieve it. This satisfies the requirements of [World Wide Web Consortium (W3C) Document Object Model (DOM) Level 1](http://go.microsoft.com/fwlink/p/?linkid=203744). The document author is responsible for implementing the functionality defined in [HTML 4.0](http://go.microsoft.com/fwlink/p/?linkid=203769) for **a** objects, if desired. You must set the value of this property before you can retrieve it. For **area** objects, the format of *p* depends on the value of the [**SHAPE**](/html/attributes/shape) attribute of the object, as follows: {

### Syntax

## See also

### Related pages

-   a[a](/html/elements/a)
-   `area`
