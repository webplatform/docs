{{Page_Title|SVG gradients}}
{{Flags
|State=Almost Ready
|Editorial notes=Fix a couple of broken links
|Checked_Out=No
}}
{{Byline}}
{{Summary_Section|This article looks at filling SVG shapes with linear and radial gradients.}}
{{Tutorial
|Content=So, perhaps more exciting than just fills and strokes, you can also create and apply gradients as either fills or strokes.
 
There are two types of gradients allowed, linear and radial ones. Linear gradients change along a straight line. To insert one, you create a <code><linearGradient></code> node inside the definitions section of your SVG file. You '''must''' give the gradient an <code>id</code> attribute, otherwise it can't be referenced by other elements inside the file, and it basically becomes a waste of space.

[[Image:SVG_Linear_Gradient_Example.png]]

<pre>&lt;?xml version="1.0" standalone="no"?&gt;

&lt;svg width="120" height="240" version="1.1" xmlns="http://www.w3.org/2000/svg"&gt;
  &lt;defs&gt;
      &lt;linearGradient id="Gradient1"&gt;
        &lt;stop class="stop1" offset="0%"/&gt;
        &lt;stop class="stop2" offset="50%"/&gt;
        &lt;stop class="stop3" offset="100%"/&gt;
      &lt;/linearGradient&gt;
      &lt;linearGradient id="Gradient2" x1="0" x2="0" y1="0" y2="1"&gt;
        &lt;stop offset="0%" stop-color="red"/&gt;
        &lt;stop offset="50%" stop-color="black" stop-opacity="0"/&gt;
        &lt;stop offset="100%" stop-color="blue"/&gt;
      &lt;/linearGradient&gt;
      &lt;style type="text/css"&gt;&lt;![CDATA[
        #rect1 { fill: url(#Gradient1); }
        .stop1 { stop-color: red; }
        .stop2 { stop-color: black; stop-opacity: 0; }
        .stop3 { stop-color: blue; }
      ]]&gt;&lt;/style&gt;
  &lt;/defs&gt;
 
  &lt;rect id="rect1" x="10" y="10" rx="15" ry="15" width="100" height="100"/&gt;
  &lt;rect x="10" y="120" rx="15" ry="15" width="100" height="100" fill="url(#Gradient2)"/&gt;
  
&lt;/svg&gt;</pre>
 
Above is an example of a linear gradient being applied to a <code>&lt;rect&gt;</code> element. Inside the linear gradient are several [[<stop>]] nodes. These nodes tell the gradient what color it should be at certain positions by specifying an <code>offset</code> attribute for the position, and a <code>stop-color</code> attribute. This can be assigned directly or through CSS. I've intermixed the two for the purposes of an example. For instance, this one tells the gradient to start at the color red, change to transparent-black in the middle, and end at the color blue. You can insert as many stop colors as you like to create a blend that's as beautiful or hideous as you need, but the offsets should always increase from 0% (or 0 if you want to drop the % sign) to 100% (or 1). Duplicate values will use the stop that is assigned furthest down the XML tree. Also, like with fill and stroke, you can specify a <code>stop-opacity</code> attribute to set the opacity at that position (again, in FF3 you can also use rgba values to do this).

<pre>&lt;stop offset="100%" stop-color="yellow" stop-opacity="0.5"/&gt;</pre>
 
To use a gradient, we have to reference it from an objects fill or stroke attributes. This is done the same way you reference elements in CSS, using a <code>url</code>. In this case, the url is just a reference to our gradient, which I've given the creative ID, "Gradient". So to attach it we just set the fill to <code>url(#Gradient)</code>, and voila, our object is now multicolored. You can do the same with stroke.

The <code>&lt;linearGradient&gt;</code> element also takes several other attributes which specify the size and appearance of the gradient. The orientation of the gradient is controlled by two "points", designated by the attributes <code>x1</code>, <code>x2</code>, <code>y1</code>, and <code>y2</code>. These attributes define a line along which the gradient travels. The gradient defaults to a horizontal orientation, but it can be rotated by changing these. Gradient2 in the above example is designed to create a vertical gradient.
 
<pre>&lt;linearGradient id="Gradient2" x1="0" x2="0" y1="0" y2="1"&gt;</pre>

  '''Note:''' You can also use the <code>xlink:href</code> attribute on gradients too. When it is used, attributes and stops from one gradient can be included on another. In the above example, you wouldn't have to recreate all the stops in Gradient2.
  
<pre>&lt;linearGradient id="Gradient1"&gt;
   &lt;stop id="stop1" offset="0%"/&gt;
   &lt;stop id="stop2" offset="50%"/&gt;
   &lt;stop id="stop3" offset="100%"/&gt;
 &lt;/linearGradient&gt;
 &lt;linearGradient id="Gradient2" x1="0" x2="0" y1="0" y2="1"
    xmlns:xlink="[[http://www.w3.org/1999/xlink]]" xlink:href="#Gradient1"/&gt;</pre>

I've included the xlink namespace here directly on the node, although usually you would define it at the top of your document. More on that when we [[talk about images]]. 
Radial gradients are similar to linear ones but draw a gradient that radiates out from a point. To create one you add a [[<radialGradient>]] element to the definitions section of your document.
 
[[Image:SVG_Radial_Gradient_Example.png]]

<pre>&lt;?xml version="1.0" standalone="no"?&gt;

&lt;svg width="120" height="240" version="1.1"
  xmlns="http://www.w3.org/2000/svg"&gt;
  &lt;defs&gt;
      &lt;radialGradient id="Gradient1"&gt;
        &lt;stop offset="0%" stop-color="red"/&gt;
        &lt;stop offset="100%" stop-color="blue"/&gt;
      &lt;/radialGradient&gt;
      &lt;radialGradient id="Gradient2" cx="0.25" cy="0.25" r="0.25"&gt;
        &lt;stop offset="0%" stop-color="red"/&gt;
        &lt;stop offset="100%" stop-color="blue"/&gt;
      &lt;/radialGradient&gt;
  &lt;/defs&gt;
 
  &lt;rect x="10" y="10" rx="15" ry="15" width="100" height="100" fill="url(#Gradient1)"/&gt; 
  &lt;rect x="10" y="120" rx="15" ry="15" width="100" height="100" fill="url(#Gradient2)"/&gt; 
  
&lt;/svg&gt;</pre>
 
The stops used here are the same as before, but now the object will be red in the center, and in all directions gradually change to blue at the edge. Like linear gradients, the <code>&lt;radialGradient&gt;</code> node can take several attributes to describe its position and orientation. However, unlike linear gradients, its a bit more complex. The radial gradient, is again defined by two points, which determine where its edges are. The first of these defines a circle around which the gradient ends. It requires a center point, designated by the <code>cx</code> and <code>cy</code> attributes, and a radius, <code>r</code>. Setting these three attributes will allow you to move the gradient around and change its size, as shown in the second rect above.
 
The second point is called the focal point and is defined by the <code>fx</code> and <code>fy</code> attributes. While the first point described where the edges of the gradient were, the focal point describes where its middle is. This is easier to see with an example.
 
[[Image:SVG_Radial_Grandient_Focus_Example.png]]

<pre>&lt;?xml version="1.0" standalone="no"?&gt;

&lt;svg width="120" height="120" version="1.1"
  xmlns="http://www.w3.org/2000/svg"&gt;
  &lt;defs&gt;
      &lt;radialGradient id="Gradient"
            cx="0.5" cy="0.5" r="0.5" fx="0.25" fy="0.25"&gt;
        &lt;stop offset="0%" stop-color="red"/&gt;
        &lt;stop offset="100%" stop-color="blue"/&gt;
      &lt;/radialGradient&gt;
  &lt;/defs&gt;
 
  &lt;rect x="10" y="10" rx="15" ry="15" width="100" height="100"
        fill="url(#Gradient)" stroke="black" stroke-width="2"/&gt;

  &lt;circle cx="60" cy="60" r="50" fill="transparent" stroke="white" stroke-width="2"/&gt;
  &lt;circle cx="35" cy="35" r="2" fill="white" stroke="white"/&gt;
  &lt;circle cx="60" cy="60" r="2" fill="white" stroke="white"/&gt;
  &lt;text x="38" y="40" fill="white" font-family="sans-serif" font-size="10pt"&gt;(fx,fy)&lt;/text&gt;
  &lt;text x="63" y="63" fill="white" font-family="sans-serif" font-size="10pt"&gt;(cx,cy)&lt;/text&gt;
  
&lt;/svg&gt;</pre>
 
If the focal point is moved outside the circle described earlier, its impossible for the gradient to be rendered correctly, so the spot will be assumed to be on the edge of the circle. If the focal point isn't given at all, its assumed to be at the same place as the center point.
 
Both gradients also take a few other attributes to describe transformations and whatnot on them. The only other one I want to mention here is the <code>spreadMethod</code> attribute. This attribute controls what happens when the gradient reaches its end, but the object isn't filled yet. It can take on one of three values, "pad", "reflect", or "repeat". "Pad" is what you have seen so far. When the gradient reaches its end, the final offset color is just used to fill the rest of the object. "reflect" causes the gradient to continue on, but this take backwards, starting with the color offset at 100% and moving back to the offset at 0%, and then back up again. "Repeat" also lets the gradient keep moving, but instead of going backwards, it just jumps back to the beginning and runs again.
 
[[Image:SVG_SpreadMethod_Example.png]]

<pre>&lt;?xml version="1.0" standalone="no"?&gt;

&lt;svg width="220" height="220" version="1.1" xmlns="http://www.w3.org/2000/svg"&gt;
  &lt;defs&gt;
      &lt;radialGradient id="Gradient"
            cx="0.5" cy="0.5" r="0.25" fx=".25" fy=".25"
            spreadMethod="repeat"&gt;
        &lt;stop offset="0%" stop-color="red"/&gt;
        &lt;stop offset="100%" stop-color="blue"/&gt;
      &lt;/radialGradient&gt;
  &lt;/defs&gt;
  &lt;rect x="50" y="50" rx="15" ry="15" width="100" height="100"
       fill="url(#Gradient)"/&gt;
&lt;/svg&gt;</pre>
 
As a bit of another aside here, both gradients also have an attribute named <code>gradientUnits</code> that describes the unit system you're going to use when you describe the size or orientation of the gradient. There are two possible values to use here: <code>userSpaceOnUse</code> or <code>objectBoundingBox</code>. <code>objectBoundingBox</code> is the default so that's what I've shown so far. It essentially scales the gradient to the size of your object, so you only have to specify coordinates in values from zero to one, and they're scaled to the size of your object automatically for you. <code>userSpaceOnUse</code> essentially takes in absolute units. So you have to know where your object is, and place the gradient at the same place. The radialGradient above would be rewritten:
 
<pre>&lt;radialGradient id="Gradient" cx="60" cy="60" r="50" fx="35" fy="35" gradientUnits="userSpaceOnUse"&gt;</pre>
 
You can also then apply another transformation to the gradient by using the <code>gradientTransform</code> attribute, but since we haven't [[introduced transforms]] yet, I'll leave that for later.
 
There are some other caveats for dealing with <code>gradientUnits="objectBoundingBox"</code> when the object bounding box isn't square, but they're fairly complex and will have to wait for someone more in-the-know to explain them.
}}
{{Notes_Section}}
{{Compatibility_Section
|Not_required=Yes
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|SVG}}
{{External_Attribution
|Is_CC-BY-SA=Yes
|Sources=MDN
|MDN_link=https://developer.mozilla.org/en-US/docs/SVG/Tutorial/Gradients
|MSDN_link=
|HTML5Rocks_link=
}}