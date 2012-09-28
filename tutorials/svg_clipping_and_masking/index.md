{{Page_Title}}
{{Flags}}
{{Summary_Section|This article explains how cipping and masking work in SVG.}}
{{Tutorial
|Content=Erasing part of what one has created cumbersome might at first sight look contradictory. But when you try to create a semicircle in SVG, you will find out the use of the following properties quickly.
 
'''Clipping''' refers to removing parts of elements defined by other parts. In this case, any half-transparent effects are not possible, it's an all-or-nothing approach.
 
'''Masking''' on the other hand allows soft edges by taking transparency and grey values of the mask into account.
 
=== Creating clips ===
 
We create the above mentioned semicircle based on a <code>circle</code> element:
 
<pre>&lt;clipPath id="cut-off-bottom"&gt;
  &lt;rect x="0" y="0" width="200" height="100" /&gt;
&lt;/clipPath&gt;

&lt;circle cx="100" cy="100" r="100" clip-path="url(#cut-off-bottom)" /&gt;</pre>
 
Centered at (100,100) a circle with radius 100 is painted. The attribute <code>clip-path</code> references a <code>{{ SVGElement("clipPath") }}</code> element with a single <code>rect</code> element. This rectangular on its own would paint the upper half of the canvas black. Note, that the <code>clipPath</code> element is usually placed in a <code>defs</code> section.
 
The <code>rect</code> will not be painted, however. Instead its pixel data will be used to determine, which pixels of the circle "make it" to the final rendering. Since the rectangle covers only the upper half of the circle, the lower half of the circle will vanish:
 
[[Image:clipdemo.png]]
 
We now have a semicircle without having to deal with arcs in path elements. For the clipping, every path inside the <code>clipPath</code> is inspected and evaluated together with its stroke properties and transformation. Then every part of the target lying in a transparent area of the resulting <code>clipPath</code>'s content will not rendered. Color, opacity and such have no effect as long as they don't let parts vanish completely.
 
=== Masking ===
 
The effect of masking is most impressively presented with a gradient. If you want an element to fade out, you can achieve this effect quite quickly with masks.
 
<pre>&lt;svg version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink"&gt;
  &lt;defs&gt;
    &lt;linearGradient id="Gradient"&gt;
      &lt;stop offset="0" stop-color="white" stop-opacity="0" /&gt;
      &lt;stop offset="1" stop-color="white" stop-opacity="1" /&gt;
    &lt;/linearGradient&gt;
    &lt;mask id="Mask"&gt;
      &lt;rect x="0" y="0" width="200" height="200" fill="url(#Gradient)"  /&gt;
    &lt;/mask&gt;
  &lt;/defs&gt;

  &lt;rect x="0" y="0" width="200" height="200" fill="green" /&gt;
  &lt;rect x="0" y="0" width="200" height="200" fill="red" mask="url(#Mask)" /&gt;
&lt;/svg&gt;</pre>
 
You see a green-filled <code>rect</code> at the lowest layer and on top a red-filled <code>rect</code>. The later has the <code>mask</code> attribute pointing to the <code>mask</code> element. The content of the mask is a single <code>rect</code> element, that is filled with a transparent-to-white gradient. As a result the pixels of the red rectangle inherit the alpha value (the transparency) of the mask content, and we see a green-to-left gradient as a result:

[[Image:maskdemo.png]]

=== Transparency with opacity ===
 
There is a simple possibility to set the transparency for a whole element. It's the <code>opacity</code> attribute:
 
<pre>&lt;rect x="0" y="0" width="100" height="100" opacity=".5" /&gt;</pre>
 
The above rectangle will be painted half-transparent. For the fill and stroke there are two separate attributes, <code>fill-opacity</code> and <code>stroke-opacity</code>, that control each of those property opacities separately. Note, that the stroke will be painted on top of the filling. Hence, if you set a stroke opacity on an element, that also has a fill, the fill will shine through on half of the stroke, while on the other half the background will appear:

<pre>&lt;rect x="0" y="0" width="200" height="200" fill="blue" /&gt;
&lt;circle cx="100" cy="100" r="50" stroke="yellow" stroke-width="40" stroke-opacity=".5" fill="red" /&gt;</pre>
 
[[Image:opacitydemo.png]]
 
You see in this example the red circle on blue background. The yellow stroke is set to 50% opacity, which leads effectively to a double-color stroke.

== Using well-known CSS techniques ==
 
One of the most powerful tools in a web developer's toolbox is <code>display: none</code>. It is therefore little surprise, that it was decided to take this CSS property into SVG as well, together with <code>visibility</code> and <code>clip</code> as defined by CSS 2. For reverting a previously set <code>display: none</code> it is important to know, that the initial value for all SVG elements is <code>inline</code>.
}}
{{Compatibility_Section
|Not_required=Yes
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|SVG}}
{{External_Attribution
|Is_CC-BY-SA=Yes
|Sources=MDN
|MDN_link=https://developer.mozilla.org/en-US/docs/SVG/Tutorial/Clipping_and_masking
|MSDN_link=
|HTML5Rocks_link=
}}