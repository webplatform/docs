{{Page_Title}}
{{Flags}}
{{Summary_Section|This article shows how to add fills and strokes to the SVG shapes you have drawn.}}
{{Tutorial
|Content=So now with your knowledge of how to draw all sorts of shapes, your next goal is probably coloring them in. There are several ways to do this, including specifying attributes on the object, using inline CSS, using an embedded CSS section, or using an external CSS file. Most SVG you'll find around the web uses inline CSS, but there are advantages and disadvantages for all the types.
 
== Fill and Stroke Attributes ==
 
=== Painting ===
 
It's been a bit difficult to avoid putting some of this in your face up until now, but in case you haven't noticed, most basic coloring can be done by setting two attributes on the node: <code>fill</code> and <code>stroke</code>. Fill sets the color inside the object and stroke sets the color of the line drawn around the object. You can use the same css color naming schemes that you use in HTML, whether that's color names (that is ''red''), rgb values (that is ''rgb(255,0,0)''), hex values, rgba values, etc.

 
<pre>
 &lt;rect x="10" y="10" width="100" height="100" stroke="blue" fill="purple"
       fill-opacity="0.5" stroke-opacity="0.8"/&gt;

</pre>
 
In addition, you can specify the opacity of either the fill or stroke separately in SVG. These are controlled by the <code>fill-opacity</code> and <code>stroke-opacity</code> attributes.

 
  Note, in Firefox 3+ rgba values are also allowed, and will give the same effect, but for compatibility with other viewers, its often best to specify the fill/stroke opacity separately. If you specify both an rgba value and a fill/stroke opacity value, both will be applied. 
=== Stroke ===
 
In addition to just its color properties, there are a few other attributes available to control the way a stroke is drawn on a line.

 
[[Image:=SVG_Stroke_Linecap_Example.png|=SVG_Stroke_Linecap_Example.png]]

 
<pre>
&lt;?xml version="1.0" standalone="no"?&gt;
&lt;svg width="160" height="140" xmlns="http://www.w3.org/2000/svg" version="1.1"&gt;
  &lt;line x1="40" x2="120" y1="20" y2="20" stroke="black" stroke-width="20" stroke-linecap="butt"/&gt;
  &lt;line x1="40" x2="120" y1="60" y2="60" stroke="black" stroke-width="20" stroke-linecap="square"/&gt;
  &lt;line x1="40" x2="120" y1="100" y2="100" stroke="black" stroke-width="20" stroke-linecap="round"/&gt;
&lt;/svg&gt;
</pre>
 
Before I discuss these, I just want to note that strokes are drawn so that they are centered around the path, that is, in the example above the path is shown in pink, and the stroke in black. The <code>stroke-width</code> property defines the width of this stroke. As you can see the stroke is distributed evenly on both sides of the path.

 
The second of these is the <code>stroke-linecap</code> property, demoed above. This controls the shape shown at the end of lines. There are three possible values for it. <code>butt</code> closes the line off with a straight edge that's normal (at 90 degrees to) the direction of the stroke and crosses its end. <code>square</code> has essentially the same appearance, but stretches the stroke slightly beyond the actual path. The distance that the stroke goes beyond the path is controlled by the <code>stroke-width</code> property. <code>round</code> produces a rounded effect on the end of the stroke, The radius of this curve is, again, controlled by the stroke width.

 
There is also a property, <code>stroke-linejoin</code> to control how the line is drawn at the joint between two line segments.

 
[[Image:=SVG_Stroke_Linejoin_Example.png|=SVG_Stroke_Linejoin_Example.png]]

 
<pre>
&lt;?xml version="1.0" standalone="no"?&gt;
&lt;svg width="160" height="280" xmlns="http://www.w3.org/2000/svg" version="1.1"&gt;
  &lt;polyline points="40 60 80 20 120 60" stroke="black" stroke-width="20"
      stroke-linecap="butt" fill="none" stroke-linejoin="miter"/&gt;
  
  &lt;polyline points="40 140 80 100 120 140" stroke="black" stroke-width="20"
      stroke-linecap="round" fill="none" stroke-linejoin="round"/&gt;
  
  &lt;polyline points="40 220 80 180 120 220" stroke="black" stroke-width="20"
      stroke-linecap="square" fill="none" stroke-linejoin="bevel"/&gt;
&lt;/svg&gt;
</pre>
 
Each of these polylines have two segments. The joint where the two meet is controlled by the <code>stroke-linejoin</code> attribute. There are three possible values for this attribute. <code>miter</code> will extend the line slightly beyond its normal width to create a square corner where only one angle is used. <code>round</code>, again draws a rounded line segment. <code>bevel</code> will create a new angle to aid in the transition between the two segments.

 
Finally, you can also use dashed line types on a stroke, by specifying the <code>stroke-dasharray</code> attribute.

 
[[Image:=SVG_Stroke_Dasharray_Example.png|=SVG_Stroke_Dasharray_Example.png]]

 
<pre>
&lt;?xml version="1.0" standalone="no"?&gt;
&lt;svg width="200" height="150" xmlns="http://www.w3.org/2000/svg" version="1.1"&gt;
  &lt;path d="M 10 75 Q 50 10 100 75 T 190 75" stroke="black"
    stroke-linecap="round" stroke-dasharray="5,10,5" fill="none"/&gt;
  &lt;path d="M 10 75 L 190 75" stroke="red"
    stroke-linecap="round" stroke-width="1" stroke-dasharray="5,5" fill="none"/&gt;
&lt;/svg&gt;
</pre>
 
The <code>stroke-dasharray</code> attribute takes as an argument a series of comma separated numbers. Note, unlike paths these numbers ''must'' be comma separated. You can insert whitespace, too, if you want, but the numbers must have commas in between them. Each of the numbers specifies a distance for first the filled area, and then for the unfilled area. So in the above example, the second path fills 5 pixel units, then leaves 5 blank, then fills 5 again. You can specify more numbers if you would like a more complicated dash pattern. The first example specifies three numbers, in which case the renderer loops the numbers twice to create an even pattern. So the first path renders 5 filled, 10 empty, 5 filled, and then loops back to create 5 empty, 10 filled, 5 empty. The pattern then loops again.

 
There are a few additional stroke and fill properties available, including <code>fill-rule</code> which specifies how to color in shapes that overlap themselves, <code>stroke-miterlimit</code> which deals with a stroke should draw miters and when it shouldn't, and <code>stroke-dashoffset</code> which specifies where to start a dasharray on a line.

 
== Using CSS ==
 
In addition to setting attributes on objects, you can also use CSS to style fills and strokes on them. The syntax for this is the same as CSS used in normal HTML, except you'll be setting values like <code>fill</code> and <code>stroke</code> instead of <code>background-color</code> or <code>border</code>. I should note that not all attributes can be set via CSS. Things that deal with painting and filling are usually available, so <code>fill</code>, <code>stroke</code>, <code>stroke-dasharray</code>, etc. can all be set this way, in addition to the gradient and pattern versions of those shown below. Things like <code>width</code>, <code>height</code>, or path commands, <code>d</code>, can't be set through CSS. Its easiest just to test and find out what is available and what isn't.

 
  The [[SVG specification]] decides strictly between attributes, that are ''properties'' and other attributes. The former can be modified with CSS, the latter not. 
CSS can be inserted inline with the element via the style attribute:

 
<pre>
 &lt;rect x="10" height="180" y="10" width="180" style="stroke: black; fill: red;"/&gt;

</pre>
 
or can be moved to a special style section that you include. Instead of shoving such a section into a <code>&lt;head&gt;</code> like you do in HTML though, its included in an area called [[<defs>]]. <code>&lt;defs&gt;</code> stands for definitions, and its here where you can create elements that don't appear in the SVG directly, but are used by other elements.

 
<pre>
&lt;?xml version="1.0" standalone="no"?&gt;
&lt;svg width="200" height="200" xmlns="http://www.w3.org/2000/svg" version="1.1"&gt;
  &lt;defs&gt;
    &lt;style type="text/css"&gt;&lt;![CDATA[
       #MyRect {
         stroke: black;
         fill: red;
       }
    ]]&gt;&lt;/style&gt;
  &lt;/defs&gt;
  &lt;rect x="10" height="180" y="10" width="180" id="MyRect"/&gt;
&lt;/svg&gt;
</pre>
 
Moving styles to an area like this can make it easier to adjust properties on large groups of elements. You can also use things like the '''hover pseudo classes''' to create rollover effects:

 
<pre>
 #MyRect:hover {
   stroke: black;
   fill: blue;
 }

</pre>
 
The list could go on and on, but you're better off reading a CSS tutorial to learn about it. Some things that work in normal HTML won't work, like the <code>before</code> and <code>after</code> pseudo classes, so a bit of experimentation is needed to sort everything out.

 
You can also specify an external style sheet for your CSS rules through [[normal XML-stylesheet syntax]]:

 
<pre>
&lt;?xml version="1.0" standalone="no"?&gt;
&lt;?xml-stylesheet type="text/css" href="style.css"?&gt;

&lt;svg width="200" height="150" xmlns="http://www.w3.org/2000/svg" version="1.1"&gt;
  &lt;rect height="10" width="10" id="MyRect"/&gt;
&lt;/svg&gt;
</pre>
 
where style.css looks something like:

 
<pre>
#MyRect {
  fill: red;
  stroke: black;
}
</pre>
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|SVG}}
{{External_Attribution
|Is_CC-BY-SA=Yes
|Sources=MDN
|MDN_link=https://developer.mozilla.org/en-US/docs/SVG/Tutorial/Fills_and_Strokes
}}