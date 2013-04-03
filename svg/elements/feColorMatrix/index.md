{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic
|Content=Incomplete, Cleanup, Compatibility Incomplete, Examples Needed, Examples Best Practices
|Checked_Out=Yes
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|feColorMatrix is a filter primitive that allows the manipulation of color values across color channels. It is always a child element of a <filter> element. Using feColorMatrix, you can change color saturation, perform hue rotations, selectively adjust alpha values of particular channels, adjust contrast, brightness and more. feColorMatrix does not allow the manipulation of relative color values *within* color channels which is provided by the feComponentTransfer primitive. }}
{{Markup_Element
|DOM_interface=svg/objects/SVGFEColorMatrixElement
|Content=feColorMatrix is a filter primitive that allows the manipulation of color values across color channels. It is always a child element of a <filter> element. Using feColorMatrix, you can change color saturation, perform hue rotations, selectively adjust alpha values of particular channels, adjust contrast, brightness and more. feColorMatrix does not allow the manipulation of relative color values *within* color channels which is provided by the feComponentTransfer primitive. 

Attributes:

* in (optional): specifies the input graphic. If "in" is ommitted; and feColorMatrix is the first primitive in a filter, the default value is SourceGraphic. Otherwise, the immediately preceding primitive's result is used as input. Permitted values for "in" are described below.
* result (optional): creates a reference for the primitive's result that other primitives can use as the value of their "in" or "in2" attributes.
* color-interpolation-filters (optional): permitted values are "linearRGB" (default) and "sRGB".
* x, y, width, height (optional): default to the size of the parent filter region.

Standard SVG element attributes may also be added to the element. 

Like all filter primitives that accept an input, feColorMatrix can accept the following values as input via the "in" attribute.

* SourceGraphic: the target element(image, shape, group etc.) that references the filter
* SourceAlpha: a graphic containing just the alpha channel of the target element.
* BackgroundImage: the canvas beneath the SourceGraphic (requires a correctly specified "enable-background" attribute. (limited browser support as of Dec '12)
* BackgroundAlpha: the alpha channel of the canvas beneath the SourceGraphic (requires a correctly specified "enable-background" attribute. Limited browser support as of Dec '12)
* FillPaint: a pseudo-graphic equal to the size of the filter region filled with the fill property of the target element (limited browser support as of Dec '12)
* StrokePaint: a pseudo-graphic equal to the size of the filter region filled with the stroke property of the target element (limited browser support as of Dec '12)
* Primitive reference: the "result" of another primitive.

feColorMatrix offers four types of color manipulation: 3 shorthands and a matrix manipulation:

* saturate: adjusts the saturation of all RGB color channels (the alpha channel is not affected)
* hueRotate: adjusts the hue of all RGB color channels (the alpha channel is not affected)
* luminanceToAlpha: discards the alpha channel and replaces it with values equal to the input's luminance. The RGB channels are set to black (0,0,0).
* matrix: a superset of the shorthands. Allows the value of each channel in the output to be specified from a combination of its existing color and alpha channels.


}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===

This filter applies the following matrix transformation:

 {{!}} R' {{!}}     {{!}} a00 a01 a02 a03 a04 {{!}}   {{!}} R {{!}}
 {{!}} G' {{!}}     {{!}} a10 a11 a12 a13 a14 {{!}}   {{!}} G {{!}}
 {{!}} B' {{!}}  =  {{!}} a20 a21 a22 a23 a24 {{!}} * {{!}} B {{!}}
 {{!}} A' {{!}}     {{!}} a30 a31 a32 a33 a34 {{!}}   {{!}} A {{!}}
 {{!}} 1  {{!}}     {{!}}  0   0   0   0   1  {{!}}   {{!}} 1 {{!}}

This matrix is applied on the RGBA color and alpha values of every
pixel on the input graphics to produce a result with a new set of RGBA
color and alpha values.

The calculations are performed on non-premultiplied color values. If
the input graphics consist of premultiplied color values, those values
are automatically converted into non-premultiplied color values for
this operation.

The '''type''' attribute is used to indicate the type of matrix
operation. The keyword '''matrix''' indicates that a full 5&times;4
matrix of values will be provided. The other keywords (see
[[svg/properties/values|'''values''']]) represent convenience
shortcuts to allow commonly used color operations to be performed
without specifying a complete matrix. If the attribute '''type''' is
not specified, the effect is as if a value of '''matrix''' were
specified.
|Import_Notes====Syntax===

===Standards information===

* [http://www.w3.org/TR/SVG/filters.html#feColorMatrixElement SVG 1.1 Specification]

===Members===

The '''SVGFEColorMatrixElement''' object has these properties:

*[[svg/properties/height|'''height''']]: Gets or sets  the height of an element.
*[[svg/properties/in1|'''in1''']]: Identifies input for the given filter primitive.
*[[svg/properties/result|'''result''']]: Provides a reference for the output result of a filter.
*[[svg/properties/type (SVGFEColorMatrixElement)|'''type''']]: Indicates the type of matrix operation.
*[[svg/properties/values|'''values''']]: Numeric values for the '''feColorMatrix''' transformation matrix.
*[[svg/properties/width|'''width''']]: Defines the width of an element.
*[[svg/properties/x|'''x''']]: Gets or sets the x-coordinate value.
*[[svg/properties/y|'''y''']]: Gets or sets the y-coordinate value.
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_prefixed_supported=No
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_prefixed_supported=No
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=10
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_prefixed_supported=Yes
|Safari_supported=Yes
|Safari_version=6
|Safari_prefixed_supported=No
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=No
|Android_version=
|Android_prefixed_supported=No
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_version=Playbook OS1+, BB10
|Blackberry_prefixed_supported=No
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_prefixed_supported=No
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Unknown
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=No
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=No
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Unknown
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=No
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=No
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=iOS6
|Safari_mobile_prefixed_supported=No
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Filters, Visual Effects
}}
{{Topics|SVG}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}