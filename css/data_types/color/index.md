---
title: '<color>'
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'The &lt;color&gt; CSS data type allows for various ways of specifying a color, some of which also specify opacity.'
tags:
  - Data
  - Type
  - CSS
uri: 'css/data types/color'

---
## Summary

The &lt;color&gt; CSS data type allows for various ways of specifying a color, some of which also specify opacity.

### Syntax

Several different ways are available to specify simple color values:

-   *Keyword* values specify common color names such as **yellow**, **black**, or **transparent**. (See the table below.)

-   Hexadecimal values specify opaque colors in the range of **\#000000** (**black**) to **\#ffffff** (**white**), where each pair of characters correspond to red, green, and blue.

-   An `rgb()` function specifies red, green and blue values either as integers between 0 and 255 (corresponding to the hex values above), or as percentages. For example, `rgb(256,0,0)` and `rgb(100%,0%,0%)` both correspond to **red**.

-   An `hsl()` function specifies hue, saturation, and luminance values. Hue values are specified as an [angle within the color wheel](/css/data_types/angle) relative to **red'*, and numeric values default to degrees. Saturation specifies vividness as a percentage, with****0%**specifying various shades of gray. Luminence specifies brightness, with**0%**and**100%* corresponding to **black** and **white**, and **50%** appearing as a more vivid hue. For example, `hsl(0%,100%,50%)` also corresponds to **red**.

The following variations on the above allow you to incorporate an *alpha* channel specifying transparencies:

-   An `rgba()` function specifies red, green and blue values as described above, along with opacity expressed in decimal terms between 0 and 1. For example, `rgba(100%,0%,0%,0.5)` specifies a semi-transparent red, which would appear as pink if layered over a white background.

-   An `hsla()` function specifies hue, saturation, and luminance as described above, but with an additional *alpha* channel. For example, `hsla(0%,100%,50%,0.5)` specifies the same semi-transparent red as the `rgba()` example above.

The recently introduced **transparent** color name specifies a full transparency.

### Color Keywords

.

<table>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<thead>
<tr class="header">
<th align="left">Example</th>
<th align="left">Name</th>
<th align="left">Hex</th>
<th align="left">RGB</th>
<th align="left">HSL</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><div style="background-color: aliceblue; color: aliceblue;">
Example
</div></td>
<td align="left">aliceblue</td>
<td align="left">#f0f8ff</td>
<td align="left">rgb(94%,97%,100%)</td>
<td align="left">hsl(208,100%,97%)</td>
</tr>
<tr class="even">
<td align="left"><div style="background-color: antiquewhite; color: antiquewhite;">
Non-visible-example
</div></td>
<td align="left">antiquewhite</td>
<td align="left">#faebd7</td>
<td align="left">rgb(98%,92%,84%)</td>
<td align="left">hsl(34,78%,91%)</td>
</tr>
<tr class="odd">
<td align="left"><div style="background-color: aqua; color: aqua;">
Non-visible-example
</div></td>
<td align="left">aqua</td>
<td align="left">#00ffff</td>
<td align="left">rgb(0%,100%,100%)</td>
<td align="left">hsl(180,100%,50%)</td>
</tr>
<tr class="even">
<td align="left"><div style="background-color: aquamarine; color: aquamarine;">
Non-visible-example
</div></td>
<td align="left">aquamarine</td>
<td align="left">#7fffd4</td>
<td align="left">rgb(50%,100%,83%)</td>
<td align="left">hsl(160,100%,75%)</td>
</tr>
<tr class="odd">
<td align="left"><div style="background-color: azure; color: azure;">
Non-visible-example
</div></td>
<td align="left">azure</td>
<td align="left">#f0ffff</td>
<td align="left">rgb(94%,100%,100%)</td>
<td align="left">hsl(180,100%,97%)</td>
</tr>
<tr class="even">
<td align="left"><div style="background-color: beige; color: beige;">
Non-visible-example
</div></td>
<td align="left">beige</td>
<td align="left">#f5f5dc</td>
<td align="left">rgb(96%,96%,86%)</td>
<td align="left">hsl(60,56%,91%)</td>
</tr>
<tr class="odd">
<td align="left"><div style="background-color: bisque; color: bisque;">
Non-visible-example
</div></td>
<td align="left">bisque</td>
<td align="left">#ffe4c4</td>
<td align="left">rgb(100%,89%,77%)</td>
<td align="left">hsl(33,100%,88%)</td>
</tr>
<tr class="even">
<td align="left"><div style="background-color: black; color: black;">
Non-visible-example
</div></td>
<td align="left">black</td>
<td align="left">#000000</td>
<td align="left">rgb(0%,0%,0%)</td>
<td align="left">hsl(0,0%,0%)</td>
</tr>
<tr class="odd">
<td align="left"><div style="background-color: blanchedalmond; color: blanchedalmond;">
Non-visible-example
</div></td>
<td align="left">blanchedalmond</td>
<td align="left">#ffebcd</td>
<td align="left">rgb(100%,92%,80%)</td>
<td align="left">hsl(36,100%,90%)</td>
</tr>
<tr class="even">
<td align="left"><div style="background-color: blue; color: blue;">
Non-visible-example
</div></td>
<td align="left">blue</td>
<td align="left">#0000ff</td>
<td align="left">rgb(0%,0%,100%)</td>
<td align="left">hsl(240,100%,50%)</td>
</tr>
<tr class="odd">
<td align="left"><div style="background-color: blueviolet; color: blueviolet;">
Non-visible-example
</div></td>
<td align="left">blueviolet</td>
<td align="left">#8a2be2</td>
<td align="left">rgb(54%,17%,89%)</td>
<td align="left">hsl(271,76%,53%)</td>
</tr>
<tr class="even">
<td align="left"><div style="background-color: brown; color: brown;">
Non-visible-example
</div></td>
<td align="left">brown</td>
<td align="left">#a52a2a</td>
<td align="left">rgb(65%,16%,16%)</td>
<td align="left">hsl(0,59%,41%)</td>
</tr>
<tr class="odd">
<td align="left"><div style="background-color: burlywood; color: burlywood;">
Non-visible-example
</div></td>
<td align="left">burlywood</td>
<td align="left">#deb887</td>
<td align="left">rgb(87%,72%,53%)</td>
<td align="left">hsl(34,57%,70%)</td>
</tr>
<tr class="even">
<td align="left"><div style="background-color: cadetblue; color: cadetblue;">
Non-visible-example
</div></td>
<td align="left">cadetblue</td>
<td align="left">#5f9ea0</td>
<td align="left">rgb(37%,62%,63%)</td>
<td align="left">hsl(182,25%,50%)</td>
</tr>
<tr class="odd">
<td align="left"><div style="background-color: chartreuse; color: chartreuse;">
Non-visible-example
</div></td>
<td align="left">chartreuse</td>
<td align="left">#7fff00</td>
<td align="left">rgb(50%,100%,0%)</td>
<td align="left">hsl(90,100%,50%)</td>
</tr>
<tr class="even">
<td align="left"><div style="background-color: chocolate; color: chocolate;">
Non-visible-example
</div></td>
<td align="left">chocolate</td>
<td align="left">#d2691e</td>
<td align="left">rgb(82%,41%,12%)</td>
<td align="left">hsl(25,75%,47%)</td>
</tr>
<tr class="odd">
<td align="left"><div style="background-color: coral; color: coral;">
Non-visible-example
</div></td>
<td align="left">coral</td>
<td align="left">#ff7f50</td>
<td align="left">rgb(100%,50%,31%)</td>
<td align="left">hsl(16,100%,66%)</td>
</tr>
<tr class="even">
<td align="left"><div style="background-color: cornflowerblue; color: cornflowerblue;">
Non-visible-example
</div></td>
<td align="left">cornflowerblue</td>
<td align="left">#6495ed</td>
<td align="left">rgb(39%,58%,93%)</td>
<td align="left">hsl(219,79%,66%)</td>
</tr>
<tr class="odd">
<td align="left"><div style="background-color: cornsilk; color: cornsilk;">
Non-visible-example
</div></td>
<td align="left">cornsilk</td>
<td align="left">#fff8dc</td>
<td align="left">rgb(100%,97%,86%)</td>
<td align="left">hsl(48,100%,93%)</td>
</tr>
<tr class="even">
<td align="left"><div style="background-color: crimson; color: crimson;">
Non-visible-example
</div></td>
<td align="left">crimson</td>
<td align="left">#dc143c</td>
<td align="left">rgb(86%,8%,24%)</td>
<td align="left">hsl(348,83%,47%)</td>
</tr>
<tr class="odd">
<td align="left"><div style="background-color: cyan; color: cyan;">
Non-visible-example
</div></td>
<td align="left">cyan</td>
<td align="left">#00ffff</td>
<td align="left">rgb(0%,100%,100%)</td>
<td align="left">hsl(180,100%,50%)</td>
</tr>
<tr class="even">
<td align="left"><div style="background-color: darkblue; color: darkblue;">
Non-visible-example
</div></td>
<td align="left">darkblue</td>
<td align="left">#00008b</td>
<td align="left">rgb(0%,0%,55%)</td>
<td align="left">hsl(240,100%,27%)</td>
</tr>
<tr class="odd">
<td align="left"><div style="background-color: darkcyan; color: darkcyan;">
Non-visible-example
</div></td>
<td align="left">darkcyan</td>
<td align="left">#008b8b</td>
<td align="left">rgb(0%,55%,55%)</td>
<td align="left">hsl(180,100%,27%)</td>
</tr>
<tr class="even">
<td align="left"><div style="background-color: darkgoldenrod; color: darkgoldenrod;">
Non-visible-example
</div></td>
<td align="left">darkgoldenrod</td>
<td align="left">#b8860b</td>
<td align="left">rgb(72%,53%,4%)</td>
<td align="left">hsl(43,89%,38%)</td>
</tr>
<tr class="odd">
<td align="left"><div style="background-color: darkgray; color: darkgray;">
Non-visible-example
</div></td>
<td align="left">darkgray</td>
<td align="left">#a9a9a9</td>
<td align="left">rgb(66%,66%,66%)</td>
<td align="left">hsl(0,0%,66%)</td>
</tr>
<tr class="even">
<td align="left"><div style="background-color: darkgreen; color: darkgreen;">
Non-visible-example
</div></td>
<td align="left">darkgreen</td>
<td align="left">#006400</td>
<td align="left">rgb(0%,39%,0%)</td>
<td align="left">hsl(120,100%,20%)</td>
</tr>
<tr class="odd">
<td align="left"><div style="background-color: darkgrey; color: darkgrey;">
Non-visible-example
</div></td>
<td align="left">darkgrey</td>
<td align="left">#a9a9a9</td>
<td align="left">rgb(66%,66%,66%)</td>
<td align="left">hsl(0,0%,66%)</td>
</tr>
<tr class="even">
<td align="left"><div style="background-color: darkkhaki; color: darkkhaki;">
Non-visible-example
</div></td>
<td align="left">darkkhaki</td>
<td align="left">#bdb76b</td>
<td align="left">rgb(74%,72%,42%)</td>
<td align="left">hsl(56,38%,58%)</td>
</tr>
<tr class="odd">
<td align="left"><div style="background-color: darkmagenta; color: darkmagenta;">
Non-visible-example
</div></td>
<td align="left">darkmagenta</td>
<td align="left">#8b008b</td>
<td align="left">rgb(55%,0%,55%)</td>
<td align="left">hsl(300,100%,27%)</td>
</tr>
<tr class="even">
<td align="left"><div style="background-color: darkolivegreen; color: darkolivegreen;">
Non-visible-example
</div></td>
<td align="left">darkolivegreen</td>
<td align="left">#556b2f</td>
<td align="left">rgb(33%,42%,18%)</td>
<td align="left">hsl(82,39%,30%)</td>
</tr>
<tr class="odd">
<td align="left"><div style="background-color: darkorange; color: darkorange;">
Non-visible-example
</div></td>
<td align="left">darkorange</td>
<td align="left">#ff8c00</td>
<td align="left">rgb(100%,55%,0%)</td>
<td align="left">hsl(33,100%,50%)</td>
</tr>
<tr class="even">
<td align="left"><div style="background-color: darkorchid; color: darkorchid;">
Non-visible-example
</div></td>
<td align="left">darkorchid</td>
<td align="left">#9932cc</td>
<td align="left">rgb(60%,20%,80%)</td>
<td align="left">hsl(280,61%,50%)</td>
</tr>
<tr class="odd">
<td align="left"><div style="background-color: darkred; color: darkred;">
Non-visible-example
</div></td>
<td align="left">darkred</td>
<td align="left">#8b0000</td>
<td align="left">rgb(55%,0%,0%)</td>
<td align="left">hsl(0,100%,27%)</td>
</tr>
<tr class="even">
<td align="left"><div style="background-color: darksalmon; color: darksalmon;">
Non-visible-example
</div></td>
<td align="left">darksalmon</td>
<td align="left">#e9967a</td>
<td align="left">rgb(91%,59%,48%)</td>
<td align="left">hsl(15,72%,70%)</td>
</tr>
<tr class="odd">
<td align="left"><div style="background-color: darkseagreen; color: darkseagreen;">
Non-visible-example
</div></td>
<td align="left">darkseagreen</td>
<td align="left">#8fbc8f</td>
<td align="left">rgb(56%,74%,56%)</td>
<td align="left">hsl(120,25%,65%)</td>
</tr>
<tr class="even">
<td align="left"><div style="background-color: darkslateblue; color: darkslateblue;">
Non-visible-example
</div></td>
<td align="left">darkslateblue</td>
<td align="left">#483d8b</td>
<td align="left">rgb(28%,24%,55%)</td>
<td align="left">hsl(248,39%,39%)</td>
</tr>
<tr class="odd">
<td align="left"><div style="background-color: darkslategray; color: darkslategray;">
Non-visible-example
</div></td>
<td align="left">darkslategray</td>
<td align="left">#2f4f4f</td>
<td align="left">rgb(18%,31%,31%)</td>
<td align="left">hsl(180,25%,25%)</td>
</tr>
<tr class="even">
<td align="left"><div style="background-color: darkslategrey; color: darkslategrey;">
Non-visible-example
</div></td>
<td align="left">darkslategrey</td>
<td align="left">#2f4f4f</td>
<td align="left">rgb(18%,31%,31%)</td>
<td align="left">hsl(180,25%,25%)</td>
</tr>
<tr class="odd">
<td align="left"><div style="background-color: darkturquoise; color: darkturquoise;">
Non-visible-example
</div></td>
<td align="left">darkturquoise</td>
<td align="left">#00ced1</td>
<td align="left">rgb(0%,81%,82%)</td>
<td align="left">hsl(181,100%,41%)</td>
</tr>
<tr class="even">
<td align="left"><div style="background-color: darkviolet; color: darkviolet;">
Non-visible-example
</div></td>
<td align="left">darkviolet</td>
<td align="left">#9400d3</td>
<td align="left">rgb(58%,0%,83%)</td>
<td align="left">hsl(282,100%,41%)</td>
</tr>
<tr class="odd">
<td align="left"><div style="background-color: deeppink; color: deeppink;">
Non-visible-example
</div></td>
<td align="left">deeppink</td>
<td align="left">#ff1493</td>
<td align="left">rgb(100%,8%,58%)</td>
<td align="left">hsl(328,100%,54%)</td>
</tr>
<tr class="even">
<td align="left"><div style="background-color: deepskyblue; color: deepskyblue;">
Non-visible-example
</div></td>
<td align="left">deepskyblue</td>
<td align="left">#00bfff</td>
<td align="left">rgb(0%,75%,100%)</td>
<td align="left">hsl(195,100%,50%)</td>
</tr>
<tr class="odd">
<td align="left"><div style="background-color: dimgray; color: dimgray;">
Non-visible-example
</div></td>
<td align="left">dimgray</td>
<td align="left">#696969</td>
<td align="left">rgb(41%,41%,41%)</td>
<td align="left">hsl(0,0%,41%)</td>
</tr>
<tr class="even">
<td align="left"><div style="background-color: dimgrey; color: dimgrey;">
Non-visible-example
</div></td>
<td align="left">dimgrey</td>
<td align="left">#696969</td>
<td align="left">rgb(41%,41%,41%)</td>
<td align="left">hsl(0,0%,41%)</td>
</tr>
<tr class="odd">
<td align="left"><div style="background-color: dodgerblue; color: dodgerblue;">
Non-visible-example
</div></td>
<td align="left">dodgerblue</td>
<td align="left">#1e90ff</td>
<td align="left">rgb(12%,56%,100%)</td>
<td align="left">hsl(210,100%,56%)</td>
</tr>
<tr class="even">
<td align="left"><div style="background-color: firebrick; color: firebrick;">
Non-visible-example
</div></td>
<td align="left">firebrick</td>
<td align="left">#b22222</td>
<td align="left">rgb(70%,13%,13%)</td>
<td align="left">hsl(0,68%,42%)</td>
</tr>
<tr class="odd">
<td align="left"><div style="background-color: floralwhite; color: floralwhite;">
Non-visible-example
</div></td>
<td align="left">floralwhite</td>
<td align="left">#fffaf0</td>
<td align="left">rgb(100%,98%,94%)</td>
<td align="left">hsl(40,100%,97%)</td>
</tr>
<tr class="even">
<td align="left"><div style="background-color: forestgreen; color: forestgreen;">
Non-visible-example
</div></td>
<td align="left">forestgreen</td>
<td align="left">#228b22</td>
<td align="left">rgb(13%,55%,13%)</td>
<td align="left">hsl(120,61%,34%)</td>
</tr>
<tr class="odd">
<td align="left"><div style="background-color: fuchsia; color: fuchsia;">
Non-visible-example
</div></td>
<td align="left">fuchsia</td>
<td align="left">#ff00ff</td>
<td align="left">rgb(100%,0%,100%)</td>
<td align="left">hsl(300,100%,50%)</td>
</tr>
<tr class="even">
<td align="left"><div style="background-color: gainsboro; color: gainsboro;">
Non-visible-example
</div></td>
<td align="left">gainsboro</td>
<td align="left">#dcdcdc</td>
<td align="left">rgb(86%,86%,86%)</td>
<td align="left">hsl(0,0%,86%)</td>
</tr>
<tr class="odd">
<td align="left"><div style="background-color: ghostwhite; color: ghostwhite;">
Non-visible-example
</div></td>
<td align="left">ghostwhite</td>
<td align="left">#f8f8ff</td>
<td align="left">rgb(97%,97%,100%)</td>
<td align="left">hsl(240,100%,99%)</td>
</tr>
<tr class="even">
<td align="left"><div style="background-color: gold; color: gold;">
Non-visible-example
</div></td>
<td align="left">gold</td>
<td align="left">#ffd700</td>
<td align="left">rgb(100%,84%,0%)</td>
<td align="left">hsl(51,100%,50%)</td>
</tr>
<tr class="odd">
<td align="left"><div style="background-color: goldenrod; color: goldenrod;">
Non-visible-example
</div></td>
<td align="left">goldenrod</td>
<td align="left">#daa520</td>
<td align="left">rgb(85%,65%,13%)</td>
<td align="left">hsl(43,74%,49%)</td>
</tr>
<tr class="even">
<td align="left"><div style="background-color: gray; color: gray;">
Non-visible-example
</div></td>
<td align="left">gray</td>
<td align="left">#808080</td>
<td align="left">rgb(50%,50%,50%)</td>
<td align="left">hsl(0,0%,50%)</td>
</tr>
<tr class="odd">
<td align="left"><div style="background-color: green; color: green;">
Non-visible-example
</div></td>
<td align="left">green</td>
<td align="left">#008000</td>
<td align="left">rgb(0%,50%,0%)</td>
<td align="left">hsl(120,100%,25%)</td>
</tr>
<tr class="even">
<td align="left"><div style="background-color: greenyellow; color: greenyellow;">
Non-visible-example
</div></td>
<td align="left">greenyellow</td>
<td align="left">#adff2f</td>
<td align="left">rgb(68%,100%,18%)</td>
<td align="left">hsl(84,100%,59%)</td>
</tr>
<tr class="odd">
<td align="left"><div style="background-color: grey; color: grey;">
Non-visible-example
</div></td>
<td align="left">grey</td>
<td align="left">#808080</td>
<td align="left">rgb(50%,50%,50%)</td>
<td align="left">hsl(0,0%,50%)</td>
</tr>
<tr class="even">
<td align="left"><div style="background-color: honeydew; color: honeydew;">
Non-visible-example
</div></td>
<td align="left">honeydew</td>
<td align="left">#f0fff0</td>
<td align="left">rgb(94%,100%,94%)</td>
<td align="left">hsl(120,100%,97%)</td>
</tr>
<tr class="odd">
<td align="left"><div style="background-color: hotpink; color: hotpink;">
Non-visible-example
</div></td>
<td align="left">hotpink</td>
<td align="left">#ff69b4</td>
<td align="left">rgb(100%,41%,71%)</td>
<td align="left">hsl(330,100%,71%)</td>
</tr>
<tr class="even">
<td align="left"><div style="background-color: indianred; color: indianred;">
Non-visible-example
</div></td>
<td align="left">indianred</td>
<td align="left">#cd5c5c</td>
<td align="left">rgb(80%,36%,36%)</td>
<td align="left">hsl(0,53%,58%)</td>
</tr>
<tr class="odd">
<td align="left"><div style="background-color: indigo; color: indigo;">
Non-visible-example
</div></td>
<td align="left">indigo</td>
<td align="left">#4b0082</td>
<td align="left">rgb(29%,0%,51%)</td>
<td align="left">hsl(275,100%,25%)</td>
</tr>
<tr class="even">
<td align="left"><div style="background-color: ivory; color: ivory;">
Non-visible-example
</div></td>
<td align="left">ivory</td>
<td align="left">#fffff0</td>
<td align="left">rgb(100%,100%,94%)</td>
<td align="left">hsl(60,100%,97%)</td>
</tr>
<tr class="odd">
<td align="left"><div style="background-color: khaki; color: khaki;">
Non-visible-example
</div></td>
<td align="left">khaki</td>
<td align="left">#f0e68c</td>
<td align="left">rgb(94%,90%,55%)</td>
<td align="left">hsl(54,77%,75%)</td>
</tr>
<tr class="even">
<td align="left"><div style="background-color: lavender; color: lavender;">
Non-visible-example
</div></td>
<td align="left">lavender</td>
<td align="left">#e6e6fa</td>
<td align="left">rgb(90%,90%,98%)</td>
<td align="left">hsl(240,67%,94%)</td>
</tr>
<tr class="odd">
<td align="left"><div style="background-color: lavenderblush; color: lavenderblush;">
Non-visible-example
</div></td>
<td align="left">lavenderblush</td>
<td align="left">#fff0f5</td>
<td align="left">rgb(100%,94%,96%)</td>
<td align="left">hsl(340,100%,97%)</td>
</tr>
<tr class="even">
<td align="left"><div style="background-color: lawngreen; color: lawngreen;">
Non-visible-example
</div></td>
<td align="left">lawngreen</td>
<td align="left">#7cfc00</td>
<td align="left">rgb(49%,99%,0%)</td>
<td align="left">hsl(90,100%,49%)</td>
</tr>
<tr class="odd">
<td align="left"><div style="background-color: lemonchiffon; color: lemonchiffon;">
Non-visible-example
</div></td>
<td align="left">lemonchiffon</td>
<td align="left">#fffacd</td>
<td align="left">rgb(100%,98%,80%)</td>
<td align="left">hsl(54,100%,90%)</td>
</tr>
<tr class="even">
<td align="left"><div style="background-color: lightblue; color: lightblue;">
Non-visible-example
</div></td>
<td align="left">lightblue</td>
<td align="left">#add8e6</td>
<td align="left">rgb(68%,85%,90%)</td>
<td align="left">hsl(195,53%,79%)</td>
</tr>
<tr class="odd">
<td align="left"><div style="background-color: lightcoral; color: lightcoral;">
Non-visible-example
</div></td>
<td align="left">lightcoral</td>
<td align="left">#f08080</td>
<td align="left">rgb(94%,50%,50%)</td>
<td align="left">hsl(0,79%,72%)</td>
</tr>
<tr class="even">
<td align="left"><div style="background-color: lightcyan; color: lightcyan;">
Non-visible-example
</div></td>
<td align="left">lightcyan</td>
<td align="left">#e0ffff</td>
<td align="left">rgb(88%,100%,100%)</td>
<td align="left">hsl(180,100%,94%)</td>
</tr>
<tr class="odd">
<td align="left"><div style="background-color: lightgoldenrodyellow; color: lightgoldenrodyellow;">
Non-visible-example
</div></td>
<td align="left">lightgoldenrodyellow</td>
<td align="left">#fafad2</td>
<td align="left">rgb(98%,98%,82%)</td>
<td align="left">hsl(60,80%,90%)</td>
</tr>
<tr class="even">
<td align="left"><div style="background-color: lightgray; color: lightgray;">
Non-visible-example
</div></td>
<td align="left">lightgray</td>
<td align="left">#d3d3d3</td>
<td align="left">rgb(83%,83%,83%)</td>
<td align="left">hsl(0,0%,83%)</td>
</tr>
<tr class="odd">
<td align="left"><div style="background-color: lightgreen; color: lightgreen;">
Non-visible-example
</div></td>
<td align="left">lightgreen</td>
<td align="left">#90ee90</td>
<td align="left">rgb(56%,93%,56%)</td>
<td align="left">hsl(120,73%,75%)</td>
</tr>
<tr class="even">
<td align="left"><div style="background-color: lightgrey; color: lightgrey;">
Non-visible-example
</div></td>
<td align="left">lightgrey</td>
<td align="left">#d3d3d3</td>
<td align="left">rgb(83%,83%,83%)</td>
<td align="left">hsl(0,0%,83%)</td>
</tr>
<tr class="odd">
<td align="left"><div style="background-color: lightpink; color: lightpink;">
Non-visible-example
</div></td>
<td align="left">lightpink</td>
<td align="left">#ffb6c1</td>
<td align="left">rgb(100%,71%,76%)</td>
<td align="left">hsl(351,100%,86%)</td>
</tr>
<tr class="even">
<td align="left"><div style="background-color: lightsalmon; color: lightsalmon;">
Non-visible-example
</div></td>
<td align="left">lightsalmon</td>
<td align="left">#ffa07a</td>
<td align="left">rgb(100%,63%,48%)</td>
<td align="left">hsl(17,100%,74%)</td>
</tr>
<tr class="odd">
<td align="left"><div style="background-color: lightseagreen; color: lightseagreen;">
Non-visible-example
</div></td>
<td align="left">lightseagreen</td>
<td align="left">#20b2aa</td>
<td align="left">rgb(13%,70%,67%)</td>
<td align="left">hsl(177,70%,41%)</td>
</tr>
<tr class="even">
<td align="left"><div style="background-color: lightskyblue; color: lightskyblue;">
Non-visible-example
</div></td>
<td align="left">lightskyblue</td>
<td align="left">#87cefa</td>
<td align="left">rgb(53%,81%,98%)</td>
<td align="left">hsl(203,92%,75%)</td>
</tr>
<tr class="odd">
<td align="left"><div style="background-color: lightslategray; color: lightslategray;">
Non-visible-example
</div></td>
<td align="left">lightslategray</td>
<td align="left">#778899</td>
<td align="left">rgb(47%,53%,60%)</td>
<td align="left">hsl(210,14%,53%)</td>
</tr>
<tr class="even">
<td align="left"><div style="background-color: lightslategrey; color: lightslategrey;">
Non-visible-example
</div></td>
<td align="left">lightslategrey</td>
<td align="left">#778899</td>
<td align="left">rgb(47%,53%,60%)</td>
<td align="left">hsl(210,14%,53%)</td>
</tr>
<tr class="odd">
<td align="left"><div style="background-color: lightsteelblue; color: lightsteelblue;">
Non-visible-example
</div></td>
<td align="left">lightsteelblue</td>
<td align="left">#b0c4de</td>
<td align="left">rgb(69%,77%,87%)</td>
<td align="left">hsl(214,41%,78%)</td>
</tr>
<tr class="even">
<td align="left"><div style="background-color: lightyellow; color: lightyellow;">
Non-visible-example
</div></td>
<td align="left">lightyellow</td>
<td align="left">#ffffe0</td>
<td align="left">rgb(100%,100%,88%)</td>
<td align="left">hsl(60,100%,94%)</td>
</tr>
<tr class="odd">
<td align="left"><div style="background-color: lime; color: lime;">
Non-visible-example
</div></td>
<td align="left">lime</td>
<td align="left">#00ff00</td>
<td align="left">rgb(0%,100%,0%)</td>
<td align="left">hsl(120,100%,50%)</td>
</tr>
<tr class="even">
<td align="left"><div style="background-color: limegreen; color: limegreen;">
Non-visible-example
</div></td>
<td align="left">limegreen</td>
<td align="left">#32cd32</td>
<td align="left">rgb(20%,80%,20%)</td>
<td align="left">hsl(120,61%,50%)</td>
</tr>
<tr class="odd">
<td align="left"><div style="background-color: linen; color: linen;">
Non-visible-example
</div></td>
<td align="left">linen</td>
<td align="left">#faf0e6</td>
<td align="left">rgb(98%,94%,90%)</td>
<td align="left">hsl(30,67%,94%)</td>
</tr>
<tr class="even">
<td align="left"><div style="background-color: magenta; color: magenta;">
Non-visible-example
</div></td>
<td align="left">magenta</td>
<td align="left">#ff00ff</td>
<td align="left">rgb(100%,0%,100%)</td>
<td align="left">hsl(300,100%,50%)</td>
</tr>
<tr class="odd">
<td align="left"><div style="background-color: maroon; color: maroon;">
Non-visible-example
</div></td>
<td align="left">maroon</td>
<td align="left">#800000</td>
<td align="left">rgb(50%,0%,0%)</td>
<td align="left">hsl(0,100%,25%)</td>
</tr>
<tr class="even">
<td align="left"><div style="background-color: mediumaquamarine; color: mediumaquamarine;">
Non-visible-example
</div></td>
<td align="left">mediumaquamarine</td>
<td align="left">#66cdaa</td>
<td align="left">rgb(40%,80%,67%)</td>
<td align="left">hsl(160,51%,60%)</td>
</tr>
<tr class="odd">
<td align="left"><div style="background-color: mediumblue; color: mediumblue;">
Non-visible-example
</div></td>
<td align="left">mediumblue</td>
<td align="left">#0000cd</td>
<td align="left">rgb(0%,0%,80%)</td>
<td align="left">hsl(240,100%,40%)</td>
</tr>
<tr class="even">
<td align="left"><div style="background-color: mediumorchid; color: mediumorchid;">
Non-visible-example
</div></td>
<td align="left">mediumorchid</td>
<td align="left">#ba55d3</td>
<td align="left">rgb(73%,33%,83%)</td>
<td align="left">hsl(288,59%,58%)</td>
</tr>
<tr class="odd">
<td align="left"><div style="background-color: mediumpurple; color: mediumpurple;">
Non-visible-example
</div></td>
<td align="left">mediumpurple</td>
<td align="left">#9370db</td>
<td align="left">rgb(58%,44%,86%)</td>
<td align="left">hsl(260,60%,65%)</td>
</tr>
<tr class="even">
<td align="left"><div style="background-color: mediumseagreen; color: mediumseagreen;">
Non-visible-example
</div></td>
<td align="left">mediumseagreen</td>
<td align="left">#3cb371</td>
<td align="left">rgb(24%,70%,44%)</td>
<td align="left">hsl(147,50%,47%)</td>
</tr>
<tr class="odd">
<td align="left"><div style="background-color: mediumslateblue; color: mediumslateblue;">
Non-visible-example
</div></td>
<td align="left">mediumslateblue</td>
<td align="left">#7b68ee</td>
<td align="left">rgb(48%,41%,93%)</td>
<td align="left">hsl(249,80%,67%)</td>
</tr>
<tr class="even">
<td align="left"><div style="background-color: mediumspringgreen; color: mediumspringgreen;">
Non-visible-example
</div></td>
<td align="left">mediumspringgreen</td>
<td align="left">#00fa9a</td>
<td align="left">rgb(0%,98%,60%)</td>
<td align="left">hsl(157,100%,49%)</td>
</tr>
<tr class="odd">
<td align="left"><div style="background-color: mediumturquoise; color: mediumturquoise;">
Non-visible-example
</div></td>
<td align="left">mediumturquoise</td>
<td align="left">#48d1cc</td>
<td align="left">rgb(28%,82%,80%)</td>
<td align="left">hsl(178,60%,55%)</td>
</tr>
<tr class="even">
<td align="left"><div style="background-color: mediumvioletred; color: mediumvioletred;">
Non-visible-example
</div></td>
<td align="left">mediumvioletred</td>
<td align="left">#c71585</td>
<td align="left">rgb(78%,8%,52%)</td>
<td align="left">hsl(322,81%,43%)</td>
</tr>
<tr class="odd">
<td align="left"><div style="background-color: midnightblue; color: midnightblue;">
Non-visible-example
</div></td>
<td align="left">midnightblue</td>
<td align="left">#191970</td>
<td align="left">rgb(10%,10%,44%)</td>
<td align="left">hsl(240,64%,27%)</td>
</tr>
<tr class="even">
<td align="left"><div style="background-color: mintcream; color: mintcream;">
Non-visible-example
</div></td>
<td align="left">mintcream</td>
<td align="left">#f5fffa</td>
<td align="left">rgb(96%,100%,98%)</td>
<td align="left">hsl(150,100%,98%)</td>
</tr>
<tr class="odd">
<td align="left"><div style="background-color: mistyrose; color: mistyrose;">
Non-visible-example
</div></td>
<td align="left">mistyrose</td>
<td align="left">#ffe4e1</td>
<td align="left">rgb(100%,89%,88%)</td>
<td align="left">hsl(6,100%,94%)</td>
</tr>
<tr class="even">
<td align="left"><div style="background-color: moccasin; color: moccasin;">
Non-visible-example
</div></td>
<td align="left">moccasin</td>
<td align="left">#ffe4b5</td>
<td align="left">rgb(100%,89%,71%)</td>
<td align="left">hsl(38,100%,85%)</td>
</tr>
<tr class="odd">
<td align="left"><div style="background-color: navajowhite; color: navajowhite;">
Non-visible-example
</div></td>
<td align="left">navajowhite</td>
<td align="left">#ffdead</td>
<td align="left">rgb(100%,87%,68%)</td>
<td align="left">hsl(36,100%,84%)</td>
</tr>
<tr class="even">
<td align="left"><div style="background-color: navy; color: navy;">
Non-visible-example
</div></td>
<td align="left">navy</td>
<td align="left">#000080</td>
<td align="left">rgb(0%,0%,50%)</td>
<td align="left">hsl(240,100%,25%)</td>
</tr>
<tr class="odd">
<td align="left"><div style="background-color: oldlace; color: oldlace;">
Non-visible-example
</div></td>
<td align="left">oldlace</td>
<td align="left">#fdf5e6</td>
<td align="left">rgb(99%,96%,90%)</td>
<td align="left">hsl(39,85%,95%)</td>
</tr>
<tr class="even">
<td align="left"><div style="background-color: olive; color: olive;">
Non-visible-example
</div></td>
<td align="left">olive</td>
<td align="left">#808000</td>
<td align="left">rgb(50%,50%,0%)</td>
<td align="left">hsl(60,100%,25%)</td>
</tr>
<tr class="odd">
<td align="left"><div style="background-color: olivedrab; color: olivedrab;">
Non-visible-example
</div></td>
<td align="left">olivedrab</td>
<td align="left">#6b8e23</td>
<td align="left">rgb(42%,56%,14%)</td>
<td align="left">hsl(80,60%,35%)</td>
</tr>
<tr class="even">
<td align="left"><div style="background-color: orange; color: orange;">
Non-visible-example
</div></td>
<td align="left">orange</td>
<td align="left">#ffa500</td>
<td align="left">rgb(100%,65%,0%)</td>
<td align="left">hsl(39,100%,50%)</td>
</tr>
<tr class="odd">
<td align="left"><div style="background-color: orangered; color: orangered;">
Non-visible-example
</div></td>
<td align="left">orangered</td>
<td align="left">#ff4500</td>
<td align="left">rgb(100%,27%,0%)</td>
<td align="left">hsl(16,100%,50%)</td>
</tr>
<tr class="even">
<td align="left"><div style="background-color: orchid; color: orchid;">
Non-visible-example
</div></td>
<td align="left">orchid</td>
<td align="left">#da70d6</td>
<td align="left">rgb(85%,44%,84%)</td>
<td align="left">hsl(302,59%,65%)</td>
</tr>
<tr class="odd">
<td align="left"><div style="background-color: palegoldenrod; color: palegoldenrod;">
Non-visible-example
</div></td>
<td align="left">palegoldenrod</td>
<td align="left">#eee8aa</td>
<td align="left">rgb(93%,91%,67%)</td>
<td align="left">hsl(55,67%,80%)</td>
</tr>
<tr class="even">
<td align="left"><div style="background-color: palegreen; color: palegreen;">
Non-visible-example
</div></td>
<td align="left">palegreen</td>
<td align="left">#98fb98</td>
<td align="left">rgb(60%,98%,60%)</td>
<td align="left">hsl(120,93%,79%)</td>
</tr>
<tr class="odd">
<td align="left"><div style="background-color: paleturquoise; color: paleturquoise;">
Non-visible-example
</div></td>
<td align="left">paleturquoise</td>
<td align="left">#afeeee</td>
<td align="left">rgb(69%,93%,93%)</td>
<td align="left">hsl(180,65%,81%)</td>
</tr>
<tr class="even">
<td align="left"><div style="background-color: palevioletred; color: palevioletred;">
Non-visible-example
</div></td>
<td align="left">palevioletred</td>
<td align="left">#db7093</td>
<td align="left">rgb(86%,44%,58%)</td>
<td align="left">hsl(340,60%,65%)</td>
</tr>
<tr class="odd">
<td align="left"><div style="background-color: papayawhip; color: papayawhip;">
Non-visible-example
</div></td>
<td align="left">papayawhip</td>
<td align="left">#ffefd5</td>
<td align="left">rgb(100%,94%,84%)</td>
<td align="left">hsl(37,100%,92%)</td>
</tr>
<tr class="even">
<td align="left"><div style="background-color: peachpuff; color: peachpuff;">
Non-visible-example
</div></td>
<td align="left">peachpuff</td>
<td align="left">#ffdab9</td>
<td align="left">rgb(100%,85%,73%)</td>
<td align="left">hsl(28,100%,86%)</td>
</tr>
<tr class="odd">
<td align="left"><div style="background-color: peru; color: peru;">
Non-visible-example
</div></td>
<td align="left">peru</td>
<td align="left">#cd853f</td>
<td align="left">rgb(80%,52%,25%)</td>
<td align="left">hsl(30,59%,53%)</td>
</tr>
<tr class="even">
<td align="left"><div style="background-color: pink; color: pink;">
Non-visible-example
</div></td>
<td align="left">pink</td>
<td align="left">#ffc0cb</td>
<td align="left">rgb(100%,75%,80%)</td>
<td align="left">hsl(350,100%,88%)</td>
</tr>
<tr class="odd">
<td align="left"><div style="background-color: plum; color: plum;">
Non-visible-example
</div></td>
<td align="left">plum</td>
<td align="left">#dda0dd</td>
<td align="left">rgb(87%,63%,87%)</td>
<td align="left">hsl(300,47%,75%)</td>
</tr>
<tr class="even">
<td align="left"><div style="background-color: powderblue; color: powderblue;">
Non-visible-example
</div></td>
<td align="left">powderblue</td>
<td align="left">#b0e0e6</td>
<td align="left">rgb(69%,88%,90%)</td>
<td align="left">hsl(187,52%,80%)</td>
</tr>
<tr class="odd">
<td align="left"><div style="background-color: purple; color: purple;">
Non-visible-example
</div></td>
<td align="left">purple</td>
<td align="left">#800080</td>
<td align="left">rgb(50%,0%,50%)</td>
<td align="left">hsl(300,100%,25%)</td>
</tr>
<tr class="even">
<td align="left"><div style="background-color: red; color: red;">
Non-visible-example
</div></td>
<td align="left">red</td>
<td align="left">#ff0000</td>
<td align="left">rgb(100%,0%,0%)</td>
<td align="left">hsl(0,100%,50%)</td>
</tr>
<tr class="odd">
<td align="left"><div style="background-color: rosybrown; color: rosybrown;">
Non-visible-example
</div></td>
<td align="left">rosybrown</td>
<td align="left">#bc8f8f</td>
<td align="left">rgb(74%,56%,56%)</td>
<td align="left">hsl(0,25%,65%)</td>
</tr>
<tr class="even">
<td align="left"><div style="background-color: royalblue; color: royalblue;">
Non-visible-example
</div></td>
<td align="left">royalblue</td>
<td align="left">#4169e1</td>
<td align="left">rgb(25%,41%,88%)</td>
<td align="left">hsl(225,73%,57%)</td>
</tr>
<tr class="odd">
<td align="left"><div style="background-color: saddlebrown; color: saddlebrown;">
Non-visible-example
</div></td>
<td align="left">saddlebrown</td>
<td align="left">#8b4513</td>
<td align="left">rgb(55%,27%,7%)</td>
<td align="left">hsl(25,76%,31%)</td>
</tr>
<tr class="even">
<td align="left"><div style="background-color: salmon; color: salmon;">
Non-visible-example
</div></td>
<td align="left">salmon</td>
<td align="left">#fa8072</td>
<td align="left">rgb(98%,50%,45%)</td>
<td align="left">hsl(6,93%,71%)</td>
</tr>
<tr class="odd">
<td align="left"><div style="background-color: sandybrown; color: sandybrown;">
Non-visible-example
</div></td>
<td align="left">sandybrown</td>
<td align="left">#f4a460</td>
<td align="left">rgb(96%,64%,38%)</td>
<td align="left">hsl(28,87%,67%)</td>
</tr>
<tr class="even">
<td align="left"><div style="background-color: seagreen; color: seagreen;">
Non-visible-example
</div></td>
<td align="left">seagreen</td>
<td align="left">#2e8b57</td>
<td align="left">rgb(18%,55%,34%)</td>
<td align="left">hsl(146,50%,36%)</td>
</tr>
<tr class="odd">
<td align="left"><div style="background-color: seashell; color: seashell;">
Non-visible-example
</div></td>
<td align="left">seashell</td>
<td align="left">#fff5ee</td>
<td align="left">rgb(100%,96%,93%)</td>
<td align="left">hsl(25,100%,97%)</td>
</tr>
<tr class="even">
<td align="left"><div style="background-color: sienna; color: sienna;">
Non-visible-example
</div></td>
<td align="left">sienna</td>
<td align="left">#a0522d</td>
<td align="left">rgb(63%,32%,18%)</td>
<td align="left">hsl(19,56%,40%)</td>
</tr>
<tr class="odd">
<td align="left"><div style="background-color: silver; color: silver;">
Non-visible-example
</div></td>
<td align="left">silver</td>
<td align="left">#c0c0c0</td>
<td align="left">rgb(75%,75%,75%)</td>
<td align="left">hsl(0,0%,75%)</td>
</tr>
<tr class="even">
<td align="left"><div style="background-color: skyblue; color: skyblue;">
Non-visible-example
</div></td>
<td align="left">skyblue</td>
<td align="left">#87ceeb</td>
<td align="left">rgb(53%,81%,92%)</td>
<td align="left">hsl(197,71%,73%)</td>
</tr>
<tr class="odd">
<td align="left"><div style="background-color: slateblue; color: slateblue;">
Non-visible-example
</div></td>
<td align="left">slateblue</td>
<td align="left">#6a5acd</td>
<td align="left">rgb(42%,35%,80%)</td>
<td align="left">hsl(248,53%,58%)</td>
</tr>
<tr class="even">
<td align="left"><div style="background-color: slategray; color: slategray;">
Non-visible-example
</div></td>
<td align="left">slategray</td>
<td align="left">#708090</td>
<td align="left">rgb(44%,50%,56%)</td>
<td align="left">hsl(210,13%,50%)</td>
</tr>
<tr class="odd">
<td align="left"><div style="background-color: slategrey; color: slategrey;">
Non-visible-example
</div></td>
<td align="left">slategrey</td>
<td align="left">#708090</td>
<td align="left">rgb(44%,50%,56%)</td>
<td align="left">hsl(210,13%,50%)</td>
</tr>
<tr class="even">
<td align="left"><div style="background-color: snow; color: snow;">
Non-visible-example
</div></td>
<td align="left">snow</td>
<td align="left">#fffafa</td>
<td align="left">rgb(100%,98%,98%)</td>
<td align="left">hsl(0,100%,99%)</td>
</tr>
<tr class="odd">
<td align="left"><div style="background-color: springgreen; color: springgreen;">
Non-visible-example
</div></td>
<td align="left">springgreen</td>
<td align="left">#00ff7f</td>
<td align="left">rgb(0%,100%,50%)</td>
<td align="left">hsl(150,100%,50%)</td>
</tr>
<tr class="even">
<td align="left"><div style="background-color: steelblue; color: steelblue;">
Non-visible-example
</div></td>
<td align="left">steelblue</td>
<td align="left">#4682b4</td>
<td align="left">rgb(27%,51%,71%)</td>
<td align="left">hsl(207,44%,49%)</td>
</tr>
<tr class="odd">
<td align="left"><div style="background-color: tan; color: tan;">
Non-visible-example
</div></td>
<td align="left">tan</td>
<td align="left">#d2b48c</td>
<td align="left">rgb(82%,71%,55%)</td>
<td align="left">hsl(34,44%,69%)</td>
</tr>
<tr class="even">
<td align="left"><div style="background-color: teal; color: teal;">
Non-visible-example
</div></td>
<td align="left">teal</td>
<td align="left">#008080</td>
<td align="left">rgb(0%,50%,50%)</td>
<td align="left">hsl(180,100%,25%)</td>
</tr>
<tr class="odd">
<td align="left"><div style="background-color: thistle; color: thistle;">
Non-visible-example
</div></td>
<td align="left">thistle</td>
<td align="left">#d8bfd8</td>
<td align="left">rgb(85%,75%,85%)</td>
<td align="left">hsl(300,24%,80%)</td>
</tr>
<tr class="even">
<td align="left"><div style="background-color: tomato; color: tomato;">
Non-visible-example
</div></td>
<td align="left">tomato</td>
<td align="left">#ff6347</td>
<td align="left">rgb(100%,39%,28%)</td>
<td align="left">hsl(9,100%,64%)</td>
</tr>
<tr class="odd">
<td align="left"><div style="background-color: turquoise; color: turquoise;">
Non-visible-example
</div></td>
<td align="left">turquoise</td>
<td align="left">#40e0d0</td>
<td align="left">rgb(25%,88%,82%)</td>
<td align="left">hsl(174,72%,56%)</td>
</tr>
<tr class="even">
<td align="left"><div style="background-color: violet; color: violet;">
Non-visible-example
</div></td>
<td align="left">violet</td>
<td align="left">#ee82ee</td>
<td align="left">rgb(93%,51%,93%)</td>
<td align="left">hsl(300,76%,72%)</td>
</tr>
<tr class="odd">
<td align="left"><div style="background-color: wheat; color: wheat;">
Non-visible-example
</div></td>
<td align="left">wheat</td>
<td align="left">#f5deb3</td>
<td align="left">rgb(96%,87%,70%)</td>
<td align="left">hsl(39,77%,83%)</td>
</tr>
<tr class="even">
<td align="left"><div style="background-color: white; color: white;">
Non-visible-example
</div></td>
<td align="left">white</td>
<td align="left">#ffffff</td>
<td align="left">rgb(100%,100%,100%)</td>
<td align="left">hsl(0,0%,100%)</td>
</tr>
<tr class="odd">
<td align="left"><div style="background-color: whitesmoke; color: whitesmoke;">
Non-visible-example
</div></td>
<td align="left">whitesmoke</td>
<td align="left">#f5f5f5</td>
<td align="left">rgb(96%,96%,96%)</td>
<td align="left">hsl(0,0%,96%)</td>
</tr>
<tr class="even">
<td align="left"><div style="background-color: yellow; color: yellow;">
Non-visible-example
</div></td>
<td align="left">yellow</td>
<td align="left">#ffff00</td>
<td align="left">rgb(100%,100%,0%)</td>
<td align="left">hsl(60,100%,50%)</td>
</tr>
<tr class="odd">
<td align="left"><div style="background-color: yellowgreen; color: yellowgreen;">
Non-visible-example
</div></td>
<td align="left">yellowgreen</td>
<td align="left">#9acd32</td>
<td align="left">rgb(60%,80%,20%)</td>
<td align="left">hsl(80,61%,50%)</td>
</tr>
</tbody>
</table>

## Examples

``` css
aside {
    color: white;              /* white letterforms */
    text-shadow: 0 0 4px red;  /* red backlight effect */
    text-shadow: 0 0 4px rgb(100%, 0%, 0%);  /* same */
    background-color: #777777; /* gray background */
}
.semitrans {
    /* elements behind this show through */
    background-color: rgba(50%, 50%, 50%, 0.5);
}
```

## Related specifications

[CSS Values and Units Module Level 3](http://www.w3.org/TR/css3-values/)
:   Candidate Recommendation

[CSS Color Module Level 3](http://www.w3.org/TR/2011/REC-css3-color-20110607/)
:   Recommendation

[CSS 2.1](http://www.w3.org/TR/CSS21/syndata.html#color-units)
:   Recommendation

## See also

### Other articles

-   [Setting color in CSS](/tutorials/setting_color_in_css)
-   [color](/css/color)
-   [color](/css/properties/color)
