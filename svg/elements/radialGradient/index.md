{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Markup_Element
|DOM_interface=svg/objects/SVGElement
}}
{{Topics|SVG}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=In the following code example, a radial gradient fills a rectangle. The gradient is defined in a definition and fills the rectangle by referencing the gradient. The gradient runs from magenta to cyan, starting in the center with magenta and working outward to cyan.
Copy this sample to a text file and save it with the .html file extension. Run it in Internet Explorer 9 to see the circular magenta to cyan gradient filling the rectangle.

The radial-filled rectangle will look like this:
|LiveURL=
|Code=

&lt;!DOCTYPE HTML&gt;
&lt;html&gt;
	
  &lt;head&gt;
  &lt;/head&gt;
	
  &lt;body&gt;
    &lt;!-- Inline SVG --&gt;
    &lt;svg width{{=}}"400" height{{=}}"400"&gt;
      &lt;defs&gt;
        &lt;!-- Define radial gradient for magenta to cyan. --&gt;
        &lt;radialGradient id{{=}}"magenta2cyan" &gt;
        &lt;!-- First color is magenta. --&gt;
        &lt;stop offset{{=}}"0%" style{{=}}"stop-color:magenta"/&gt;
        &lt;!-- Second color is cyan. --&gt;
        &lt;stop offset{{=}}"100%" style{{=}}"stop-color:cyan"/&gt;
        &lt;/radialGradient&gt;
      &lt;/defs&gt;
      &lt;!-- Rectangle fill is defined by linear gradient in defs. --&gt;
      &lt;rect width{{=}}"100" height{{=}}"50" x{{=}}"50" y{{=}}"50"
				style{{=}}"fill:url(#magenta2cyan)"/&gt;
				
    &lt;/svg&gt;
  &lt;/body&gt;
&lt;/html&gt;
	
}}}}
{{Notes_Section
|Notes=
===Remarks===
'''Note'''  In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.
The '''radialGradient''' element inherits properties from its ancestors instead of from the element that references  the '''radialGradient''' element.
'''radialGradient''' elements are never rendered directly. They exist  so that you can reference them by  using the <code>fill</code> and <code>stroke</code> properties.
The <code>display</code> property does not apply to the '''radialGradient''' element.  '''radialGradient''' elements are not directly rendered even if the <code>display</code> property is set to a value other than <code>none</code>. But  '''radialGradient''' elements are available for referencing even when the <code>display</code> property on the '''radialGradient''' element or any of its ancestors is set to <code>none</code>.
|Import_Notes=
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}199811 Scalable Vector Graphics: Gradients and Patterns], Section 13.4.3


===Members===
The '''SVGRadialGradientElement''' object has these types of members:
*[#properties Properties]


====Properties====
The '''SVGRadialGradientElement''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[svg/properties/className|'''className''']]
|Gets  the names of the classes  that are assigned to this object.
|-
|[[svg/properties/cx (SVGRadialGradientElement)|'''cx''']]
|Gets or sets the x-coordinate for the center of the largest (that is, outermost) circle of a radial gradient.
|-
|[[svg/properties/cy (SVGRadialGradientElement)|'''cy''']]
|Gets or sets the y-coordinate for the center of the largest (that is, outermost) circle of a radial gradient.
|-
|[[svg/properties/externalResourcesRequired|'''externalResourcesRequired''']]
|Gets a value that indicates whether referenced resources that are not in the current document are required to correctly render a given element.
|-
|[[svg/properties/focusable|'''focusable''']]
|Determines if an element can acquire keyboard focus (that is, receive keyboard events) and be a target for field-to-field navigation actions (such as when  a user presses  the Tab key).
|-
|[[svg/properties/fx|'''fx''']]
|Gets or sets the x-coordinate for the focal point of a radial gradient.
|-
|[[svg/properties/fy|'''fy''']]
|Gets or sets the y-coordinate for the focal point of a radial gradient.
|-
|[[svg/properties/gradientTransform|'''gradientTransform''']]
|Gets  a value that contains the definition of an optional, additional transformation from the gradient coordinate system onto the target coordinate system.
|-
|[[svg/properties/gradientUnits|'''gradientUnits''']]
|Gets a value that indicates the type of coordinate system that is used  because  of a transformation.
|-
|[[svg/properties/href|'''href''']]
|Gets an <code>xlink:href</code> attribute of an element.
|-
|[[svg/properties/ownerSVGElement|'''ownerSVGElement''']]
|Gets the nearest ancestor [[svg/objects/SVGElement|'''svg''']] element.
|-
|[[svg/properties/r (SVGRadialGradientElement)|'''r''']]
|Gets or sets the radius of a radial gradient.
|-
|[[svg/properties/spread|'''spreadMethod''']]
|Gets a value that determines what happens if a gradient starts or ends inside the bounds of a target rectangle.
|-
|[[svg/properties/style|'''style''']]
|Gets a [[css/cssom/style|'''style''']] object.
|-
|[[svg/properties/viewportElement|'''viewportElement''']]
|Gets the element that established the current viewport.
|-
|[[svg/properties/xmlbase|'''xmlbase''']]
|Gets or sets the <code>base</code> attribute on the element.
|}
 

}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}