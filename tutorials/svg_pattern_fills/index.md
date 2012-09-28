{{Page_Title}}
{{Flags}}
{{Summary_Section|This article covers SVG pattern fills}}
{{Tutorial
|Content=Patterns, in my opinion, are one of the more confusing fill types to use in SVG. They're also very powerful, so they're worth talking about and getting at least a fundamental grasp on. Like gradients, the [[<pattern>]] element should be put in the <code>&lt;defs&gt;</code> section of your SVG file.

[[Image:SVG_Pattern_Example.png]]

<pre>&lt;?xml version="1.0" standalone="no"?&gt;
&lt;svg width="200" height="200" xmlns="http://www.w3.org/2000/svg" version="1.1"&gt;
  &lt;defs&gt;
    &lt;linearGradient id="Gradient1"&gt;
      &lt;stop offset="5%" stop-color="white"/&gt;
      &lt;stop offset="95%" stop-color="blue"/&gt;
    &lt;/linearGradient&gt;
    &lt;linearGradient id="Gradient2" x1="0" x2="0" y1="0" y2="1"&gt;
      &lt;stop offset="5%" stop-color="red"/&gt;
      &lt;stop offset="95%" stop-color="orange"/&gt;
    &lt;/linearGradient&gt;

    &lt;pattern id="Pattern" x=".05" y=".05" width=".25" height=".25"&gt;
      &lt;rect x="0" y="0" width="50" height="50" fill="skyblue"/&gt;
      &lt;rect x="0" y="0" width="25" height="25" fill="url(#Gradient2)"/&gt;
      &lt;circle cx="25" cy="25" r="20" fill="url(#Gradient1)" fill-opacity="0.5"/&gt;
    &lt;/pattern&gt; 

  &lt;/defs&gt;
  
  &lt;rect fill="url(#Pattern)" stroke="black" x="0" y="0" width="200" height="200"/&gt;
&lt;/svg&gt;</pre>
 
Inside the pattern element you can include any of the other basic shapes you've included before, and each of them can be styled using any of the styles you've learned before, including gradients and opacity. Here we've just drawn two rectangle elements inside our pattern (which overlap, and one of which is twice the size of the other and is used to fill in the entire pattern), and one circle.
 
The confusing thing about patterns is defining a unit system and their size. In the example above, we've defined a <code>width</code> and <code>height</code> attribute on the pattern element, to describe how far the pattern should go before it begins repeating itself again. There are also <code>x</code> and <code>y</code> attributes available if you want to offset the start point of this rectangle somewhere within your drawing. The reason they've been used here is described below.
 
As with the <code>gradientUnits</code> attribute used above, patterns also have an attribute, <code>patternUnits</code> which specifies the units that these attributes will take. It defaults to "objectBoundingBox" as it did above, so a value of 1 is scaled to the width/height of the object you're applying the pattern to. Since, in this case, we wanted the pattern to repeat 4 times horizontally and vertically, the height and width are set to 0.25. That means the patterns width/height is only 0.25 of the total box size.
 
Unlike gradients, patterns then have a second attribute, <code>patternContentUnits</code>, which describes the units system used inside the pattern element, on the basic shapes themselves. This attribute defaults to "userSpaceOnUse", the opposite of the <code>patternUnits</code> attribute. What this means is that unless you specify one or both of these attributes (<code>patternContentUnits</code> and <code>patternUnits</code>), the shapes you draw inside your pattern are being drawn in a different coordinate system than the pattern element is using, which can make things a bit confusing when you're writing this by hand. To make this work in the above example, we had to consider the size of our box (200 pixels) and the fact that we wanted the pattern to repeat itself 4 times horizontally and vertically. That means that each pattern unit was a 50x50 square. The two rects and the circle inside the pattern were then sized to fit in a 50x50 box. Anything that we had drawn outside that box wouldn't have been shown. The pattern also had to be offset by 10 pixels so that it would start in the upper left corner of our box, so the x and y attributes of the pattern had to be adjusted to 10/200 = 0.05.
 
The caveat here is that if the object changes size, the pattern itself will scale to fit it, but the objects inside will not. So while we would still have 4 repeating units inside the pattern, the objects composing that pattern would remain the same size, and you end up with large areas of nothing in between them. By changing the <code>patternContentUnits</code> attribute, we can put all the elements into the same unit system:
 
<pre>&lt;pattern id="Pattern" width=".25" height=".25" patternContentUnits="objectBoundingBox"&gt;
   &lt;rect x="0" y="0" width=".25" height=".25" fill="skyblue"/&gt;
   &lt;rect x="0" y="0" width=".125" height=".125" fill="url(#Gradient2)"/&gt;
   &lt;circle cx=".125" cy=".125" r=".1" fill="url(#Gradient1)" fill-opacity="0.5"/&gt;
 &lt;/pattern&gt;</pre>
 
Now, because the pattern content is in the same unit system as the pattern, we don't have to offset the box so that the pattern starts in the correct place, and if the object size was changed to a larger one, the pattern would automatically scale so that it had the same number of objects and repeats inside it. This contrasts with the "userSpaceOnUse" system, where if the object changes size the pattern would stay the same, and just repeat itself more times to fill the box.
 
As a slight aside, in Gecko circles seem to have trouble drawing if their radius is set to something less than 0.075 (even though they should be scaled up to have a much larger radius than that. This may be a bug in just the pattern element, or not a bug at all, I'm not sure). To work around that its probably best to avoid drawing in "objectBoundingBox" units unless you have to.
 
Neither of these uses is what one would normally think of when you think of a pattern. Patterns usually have a set size and repeat themselves independently of what an objects shape is. To create something like this, both the pattern and its contents must be drawn in the current userSpace, so that they don't change shape if the object does:
 
<pre> &lt;pattern id="Pattern" x="10" y="10" width="50" height="50" patternUnits="userSpaceOnUse"&gt;
   &lt;rect x="0" y="0" width="50" height="50" fill="skyblue"/&gt;
   &lt;rect x="0" y="0" width="25" height="25" fill="url(#Gradient2)"/&gt;
   &lt;circle cx="25" cy="25" r="20" fill="url(#Gradient1)" fill-opacity="0.5"/&gt;
 &lt;/pattern&gt;</pre>
 
Of course, this means that the pattern won't scale if you change your object size later. All three of the above examples are shown below on a rectangle that has been slightly elongated to a height of 300px, but I should note its not an exhaustive picture, and there are other options available depending on your application.
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
|MDN_link=https://developer.mozilla.org/en-US/docs/SVG/Tutorial/Patterns
|MSDN_link=
|HTML5Rocks_link=
}}