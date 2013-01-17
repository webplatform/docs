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

'''feConvolveMatrix''' applies a matrix convolution filter effect. A convolution combines pixels in the input image with neighboring pixels to produce a resulting image. A wide variety of imaging operations can be achieved through convolutions, including blurring, edge detection, sharpening, embossing, and beveling.

A matrix convolution is based on an ''n''-by-''m'' matrix (the convolution kernel) which describes how a given pixel value in the input image is combined with its neighboring pixel values to produce a resulting pixel value. Each result pixel is determined by applying the kernel matrix to the corresponding source pixel and its neighboring pixels.

Because they operate on pixels, matrix convolutions are inherently resolution-dependent. To make '''feConvolveMatrix''' produce resolution-independent results, an explicit value should be provided for either the [[svg/methods/setFilterRes|'''filterRes''']] attribute on the [[svg/elements/filter|'''filter''']] element and/or attribute [[svg/properties/kernelUnitLengthX|'''kernelUnitLength''']].

[[svg/properties/kernelUnitLengthX|'''kernelUnitLength''']], in combination with the other attributes, defines an implicit pixel grid in the filter effects coordinate system (that is, the coordinate system established by the [[svg/properties/primitiveUnits|'''primitiveUnits''']] attribute). If the pixel grid established by '''kernelUnitLength''' is not scaled to match the pixel grid established by attribute [[svg/methods/setFilterRes|'''filterRes''']] (implicitly or explicitly), then the input image will be temporarily rescaled to match its pixels with '''kernelUnitLength'''. The convolution happens on the resampled image. After applying the convolution, the image is resampled back to the original resolution.

|Import_Notes=

===Syntax===

===Standards information===

*[http://go.microsoft.com/fwlink/p/?linkid{{=}}226062 Scalable Vector Graphics: Filter Effects], Section 15.25.12

===Members===

The '''SVGFEConvolveMatrixElement''' object has these properties:

*[[svg/properties/bias|'''bias''']]: Shifts the range of the filter. This allows representation of values that would otherwise be clamped to 0 or 1.
*[[svg/properties/divisor|'''divisor''']]: Affects the final destination color value of the filter.
*[[svg/properties/edgeMode|'''edgeMode''']]: Determines how to extend the input image as necessary with color values so that the matrix operations can be applied when the kernel is positioned at or near the edge of the input image.
*[[svg/properties/height|'''height''']]: Gets or sets  the height of an element.
*[[svg/properties/in1|'''in1''']]: Identifies input for the given filter primitive.
*[[svg/properties/kernelMatrix|'''kernelMatrix''']]: The list of numbers that make up the kernel matrix for the convolution.
*[[svg/properties/kernelUnitLengthX|'''kernelUnitLengthX''']]: '''kernelUnitLength''' indicates the intended distance in current filter units for ''dx'' and ''dy'' in the surface normal calculation formulas.
*[[svg/properties/kernelUnitLengthY|'''kernelUnitLengthY''']]: '''kernelUnitLength''' indicates the intended distance in current filter units for ''dx'' and ''dy'' in the surface normal calculation formulas.
*[[svg/properties/orderX|'''orderX''']]: Indicates the number of cells in each dimension for [[svg/properties/kernelMatrix|'''kernelMatrix''']].
*[[svg/properties/orderY|'''orderY''']]: Indicates the number of cells in each dimension for [[svg/properties/kernelMatrix|'''kernelMatrix''']].
*[[svg/properties/preserveAlpha|'''preserveAlpha''']]: Indicates that the convolution will apply to all channels or just the color channels.
*[[svg/properties/result|'''result''']]: Provides a reference for the output result of a filter.
*[[svg/properties/targetX|'''targetX''']]: Determines the positioning in X of the convolution matrix relative to a given target pixel in the input image.
*[[svg/properties/targetY|'''targetY''']]: Determines the positioning in Y of the convolution matrix relative to a given target pixel in the input image.
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