{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Unreviewed MSDN import
|Checked_Out=No
|High-level issues=Needs Flags, Stub
}}
{{Standardization_Status|}}
{{API_Name}}
{{Topics|SVG}}
{{Notes_Section
|Notes=

===Remarks===

[[svg/elements/feTurbulence|'''SVGFETurbulenceElement''']] uses the '''type''' value to determine whether  the filter primitive should perform a '''noise''' or '''turbulence''' function. The default is  '''turbulence''' ('''turbulence''' is fractal-based and is considered smoother in appearance).

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
|Corresponds to value '''fractalNoise'''.
|-
|SVG_TURBULENCE_TYPE_TURBULENCE
|2
|Corresponds to value '''turbulence'''.
|-
|SVG_STITCHTYPE_UNKNOWN
|0
|The type is not one of the predefined types. It is invalid to attempt to define a new value of this type or to attempt to switch an existing value to this type.
|-
|SVG_STITCHTYPE_STITCH
|1
|Corresponds to value '''stitch'''.
|-
|SVG_STITCHTYPE_NOSTITCH
|2
|Corresponds to value '''noStitch'''.

|Import_Notes=

===Syntax===

}}
{{See_Also_Section
|Manual_sections=

===Related pages (MSDN)===

*[[svg/elements/feTurbulence|'''SVGFETurbulenceElement''']]
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}
[[Category:SVG]]