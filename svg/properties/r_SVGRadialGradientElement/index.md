{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following code example creates a 400 × 400 pixel viewport and draws a rectangle (of the same size) that is filled with a radial gradient that is centered at the middle of the rectangle. This radial gradient is completely white at its center and smoothly transitions to black at the end of the '''r''' radius (that is, 200 px) and beyond.  If you move the mouse pointer over the rendered rectangle, the radius of the radial gradient reduces by half; if you move the mouse pointer off the rendered rectangle, the radius returns to its original value.

'''Note'''  The '''gradientUnits{{=}}"userSpaceOnUse"''' attribute/value pair causes the radial gradient to use the current user coordinate system (of the element that references the gradient).
|LiveURL=To run the following code example, save the example by using the .svg  extension.
|Code=
&lt;?xml version{{=}}"1.0" standalone{{=}}"no"?&gt;
&lt;!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 1.1//EN" "http://www.w3.org/Graphics/SVG/1.1/DTD/svg11.dtd"&gt;
&lt;svg width{{=}}"400px" height{{=}}"400px" viewBox{{=}}"0 0 400 400" version{{=}}"1.1" xmlns{{=}}"http://www.w3.org/2000/svg"&gt;
  
  &lt;desc&gt;Fill a rectangle with a radial gradient&lt;/desc&gt;
  
  &lt;script type{{=}}"application/ecmascript"&gt;
    var radial_gradient;
    var r;
    
    window.onload {{=}} function() 
    {
      radial_gradient {{=}} document.getElementById("myGradient");
      r {{=}} parseInt(radial_gradient.getAttribute("r"));
    }
		
    function halfR() 
    {
	  radial_gradient.setAttribute("r", r/2);
    }
    
    function normalR() 
    {
	  radial_gradient.setAttribute("r", r);
    }
  &lt;/script&gt;
  
  &lt;defs&gt;
    &lt;radialGradient id{{=}}"myGradient" gradientUnits{{=}}"userSpaceOnUse" 
                    cx{{=}}"200" cy{{=}}"200" r{{=}}"200"&gt;
      &lt;stop offset{{=}}"0%" stop-color{{=}}"white" /&gt;
      &lt;stop offset{{=}}"100%" stop-color{{=}}"black" /&gt;
    &lt;/radialGradient&gt;
  &lt;/defs&gt;
  &lt;!-- The rectangle is filled by using the "myGradient" radial gradient. --&gt;
  &lt;rect fill{{=}}"url(#myGradient)" x{{=}}"0" y{{=}}"0" width{{=}}"400" height{{=}}"400" onmouseover{{=}}"halfR()" onmouseout{{=}}"normalR()"/&gt;
    
&lt;/svg&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
The '''r'''  property defines the largest (that is, the outermost) circle for a radial gradient. The gradient is drawn such that the 100% gradient stop coincides with the perimeter of this largest (that is, the outermost) circle.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}199811 Scalable Vector Graphics: Gradients and Patterns], Section 13.4.3


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[svg/elements/radialGradient|SVGRadialGradientElement]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}
[[Category:SVG]]