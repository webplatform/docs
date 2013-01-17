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
{{Notes_Section
|Notes=

===Remarks===

The Gaussian blur kernel is an approximation of the normalized convolution

G(x,y) {{=}} H(x)I(y),

where

H(x) {{=}} exp(-x<sup>2</sup>/ (2s<sup>2</sup>)) / sqrt(2* pi*s<sup>2</sup>)

and

I(y) {{=}} exp(-y<sup>2</sup>/ (2t<sup>2</sup>)) / sqrt(2* pi*t<sup>2</sup>)

with 's' being the standard deviation in the x direction and 't' being the standard deviation in the y direction, as specified by the [[svg/properties/stdDeviationX|'''stdDeviationX''']] and [[svg/properties/stdDeviationY|'''stdDeviationY''']] properties.

|Import_Notes=

===Syntax===

===Standards information===

*[http://go.microsoft.com/fwlink/p/?linkid{{=}}226062 Scalable Vector Graphics: Filter Effects], Section 15.25.19

===Members===

The '''SVGFEGaussianBlurElement''' object has these methods:

*[[svg/methods/setStdDeviation|'''setStdDeviation''']]: Sets the standard deviation values used in calculating a Gaussian blur.

The '''SVGFEGaussianBlurElement''' object has these properties:

*[[svg/properties/height|'''height''']]: Gets or sets  the height of an element.
*[[svg/properties/in1|'''in1''']]: Identifies input for the given filter primitive.
*[[svg/properties/result|'''result''']]: Provides a reference for the output result of a filter.
*[[svg/properties/stdDeviationX|'''stdDeviationX''']]: Gets a value that indicates the standard deviation in the x-direction, used in calculating a Gaussian blur.
*[[svg/properties/stdDeviationY|'''stdDeviationY''']]: Gets a value that indicates the standard deviation in the y-direction, used in calculating a Gaussian blur.
*[[svg/properties/width|'''width''']]: Defines the width of an element.
*[[svg/properties/x|'''x''']]: Gets or sets the x-coordinate value.
*[[svg/properties/y|'''y''']]: Gets or sets the y-coordinate value.

}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}