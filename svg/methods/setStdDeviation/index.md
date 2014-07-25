{{Page Title}}
{{Flags
|State=Not Ready
|Editorial notes=Stub
}}
{{Standardization_Status|}}
{{API_Name}}
{{Topics|SVG}}
{{Notes_Section
|Notes=

===Remarks===

If two values are provided, the first value represents a standard deviation value along the x-axis of the coordinate system established by the [[svg/properties/primitiveUnits|'''primitiveUnits''']] attribute on the [[svg/elements/filter|'''filter''']] element. The second value represents a standard deviation along the y-axis.

If one number is provided, then that value is used for both ''stdDeviationX'' and ''stdDeviationY''.
Negative values are not allowed.

A value of zero disables the effect of the given filter primitive (that is, the result is the filter input image). If the '''stdDeviation''' method is zero in only one of ''stdDeviationX'' or ''stdDeviationY'', then the effect is that the blur is applied only in the direction that has a non-zero value.

If the '''stdDeviation''' method is not specified, then the effect is as if a value of zero were specified.
|Import_Notes=

===Syntax===

===Standards information===

*[http://go.microsoft.com/fwlink/p/?linkid{{=}}226062 Scalable Vector Graphics: Filter Effects], Section 15.25.19

}}
{{See_Also_Section
|Manual_sections=

===Related pages (MSDN)===

*[[svg/elements/feGaussianBlur|'''SVGFEGaussianBlurElement''']]
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}

[[Category:SVG]]