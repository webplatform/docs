{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|The text-shadow property adds shadows to text. It accepts a comma-separated list of shadows to be applied to the text and [[css/properties/text-decoration|text-decorations]] of the element.}}
{{CSS Property
|Initial value=none
|Applies to=All elements and generated content
|Inherited=Yes
|Media=visual
|Computed value=as specified
|Animatable=Yes
|CSS object model property=textShadow
|Values={{CSS Property Value
|Data Type=none
|Description=Default. Indicates there is no shadow.
}}{{CSS Property Value
|Data Type=<color>
|Description=Optional. See [[css/color|CSS color values]] for possible keywords and notations. If not specified, the color used depends on the browser. The color value can be specified either before or after the offset values.
}}{{CSS Property Value
|Data Type=<offset-x> <offset-y>
|Description=Required. Two [[css/data_types/length|<length>]] values that specify the shadow's distance from the text. 
The first is the horizontal distance, with positive values moving it to the right, and negative values moving it to the left.
The secont is the vertical distance, with positive values moving the shadow down, and negative values moving it up.
}}{{CSS Property Value
|Data Type=<blur-radius>
|Description=Optional. The blur radius is a [[css/data_types/length|<length>]] value that indicates the boundaries of the blur effect. Defaults to 0.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=The following example applies a dark gray shadow with a small blur value slightly to the right and under the specified text:
|Code=.myselector 
{
  text-shadow: 0.1em 0.1em 0.15em #333;
}
}}
}}
{{Notes_Section
|Notes=The '''text-shadow''' property can specify one or more drop shadows. The components of each shadow are interpreted as follows:
*Required: The first length is the ''horizontal offset'' of the shadow. A positive value draws a shadow that is offset to the right of the box, a negative length to the left.
*Required: The second length is the ''vertical offset''. A positive value offsets the shadow down, a negative one up.
*Optional: The third length is a ''blur distance''. Negative values are not allowed. If the blur value is zero, the shadow's edge is sharp. Otherwise, the larger the value, the more the shadow's edge is blurred.
*Optional: The fourth length is a ''spread distance''. Positive values cause the shadow shape to expand in all directions by the specified radius. Negative values cause the shadow shape to contract.
*Optional: The ''color'' is the color of the shadow.
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=2.0.158.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=3.5
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=10
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=9.5
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=1.1
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Text
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}