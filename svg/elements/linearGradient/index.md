{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Needs summary, spec reference, standardization status
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{Markup_Element
|DOM_interface=svg/objects/SVGElement
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=In the following code example, a linear gradient fills a rectangle. The gradient is defined in a definition and fills the rectangle by referencing the gradient. The gradient runs from magenta to cyan.

Copy this sample to a text file and save it with the ''.html'' file extension. Run it in Internet Explorer 9 to see the magenta-to-cyan gradient-filled rectangle.

The gradient-filled rectangle will look like this:
|Code=<syntaxhighlight lang="xml">
<!DOCTYPE HTML>
<html>
  <head></head>
  <body>
    <!-- Inline SVG -->
    <svg width="400" height="400">
      <defs>
        <!-- Define linear gradient for magenta to cyan. -->
        <linearGradient id="magenta2cyan" >
        <!-- First color is magenta. -->
        <stop offset="0%" style="stop-color:magenta"/>
        <!-- Second color is cyan. -->
        <stop offset="100%" style="stop-color:cyan"/>
        </linearGradient>
      </defs>
      <!-- Rectangle fill is defined by linear gradient in defs. -->
      <rect width="100" height="50" x="50" y="50" style="fill:url(#magenta2cyan)"/>
    </svg>
  </body>
</html>
</syntaxhighlight>
}}
}}
{{Notes_Section
|Notes====Remarks===

'''Note:'''  In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.
|Import_Notes====Standards information===

*[http://go.microsoft.com/fwlink/p/?linkid{{=}}199811 Scalable Vector Graphics: Gradients and Patterns], Section 13.4.2

===Members===

The '''SVGLinearGradientElement''' object has these properties:

*[[svg/properties/className|'''className''']]: Gets  the names of the classes  that are assigned to this object.
*[[svg/properties/externalResourcesRequired|'''externalResourcesRequired''']]: Gets a value that indicates whether referenced resources that are not in the current document are required to correctly render a given element.
*[[svg/properties/focusable|'''focusable''']]: Determines if an element can acquire keyboard focus (that is, receive keyboard events) and be a target for field-to-field navigation actions (such as when  a user presses  the Tab key).
*[[svg/properties/gradientTransform|'''gradientTransform''']]: Gets  a value that contains the definition of an optional, additional transformation from the gradient coordinate system onto the target coordinate system.
*[[svg/properties/gradientUnits|'''gradientUnits''']]: Gets a value that indicates the type of coordinate system that is used  because  of a transformation.
*[[svg/properties/href|'''href''']]: Gets an '''xlink:href''' attribute of an element.
*[[svg/properties/ownerSVGElement|'''ownerSVGElement''']]: Gets the nearest ancestor [[svg/objects/SVGElement|'''svg''']] element.
*[[svg/properties/spread|'''spreadMethod''']]: Gets a value that determines what happens if a gradient starts or ends inside the bounds of a target rectangle.
*[[svg/properties/style|'''style''']]: Gets a [[css/cssom/style|'''style''']] object.
*[[svg/properties/viewportElement|'''viewportElement''']]: Gets the element that established the current viewport.
*[[svg/properties/x1 (SVGLinearGradientElement)|'''x1''']]: Gets or sets the x-coordinate for the begining of a gradient vector.
*[[svg/properties/x2 (SVGLinearGradientElement)|'''x2''']]: Gets or sets the x-coordinate for the end of a gradient vector.
*[[svg/properties/xmlbase|'''xmlbase''']]: Gets or sets the '''base''' attribute on the element.
*[[svg/properties/y1 (SVGLinearGradientElement)|'''y1''']]: Gets or sets the y-coordinate for the begining of a gradient vector.
*[[svg/properties/y2 (SVGLinearGradientElement)|'''y2''']]: Gets or sets the y-coordinate for the end of a gradient vector.
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|SVG}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}