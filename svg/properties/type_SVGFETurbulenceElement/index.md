{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Notes_Section
|Notes=
===Remarks===
[[svg/elements/feTurbulence|'''SVGFETurbulenceElement''']] uses the '''type''' value to determine whether  the filter primitive should perform a <code>noise</code> or <code>turbulence</code> function. The default is  <code>turbulence</code> (<code>turbulence</code> is fractal-based and is considered smoother in appearance).
The following are constants associated with [[svg/elements/feTurbulence|'''SVGFETurbulenceElement''']].
{| class="wikitable"
|-
!Constant
!Value
!Description
|-
|SVG_TURBULENCE_TYPE_UNKNOWN
|0
|The type is not one of the predefined types. It is invalid to attempt to define a new value of this type or to attempt to switch an existing value to this type.
|-
|SVG_TURBULENCE_TYPE_FRACTALNOISE
|1
|Corresponds to value <code>fractalNoise</code>.
|-
|SVG_TURBULENCE_TYPE_TURBULENCE
|2
|Corresponds to value <code>turbulence</code>.
|-
|SVG_STITCHTYPE_UNKNOWN
|0
|The type is not one of the predefined types. It is invalid to attempt to define a new value of this type or to attempt to switch an existing value to this type.
|-
|SVG_STITCHTYPE_STITCH
|1
|Corresponds to value <code>stitch</code>.
|-
|SVG_STITCHTYPE_NOSTITCH
|2
|Corresponds to value <code>noStitch</code>.
|}
 
|Import_Notes=
===Syntax===
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[svg/elements/feTurbulence|SVGFETurbulenceElement]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}