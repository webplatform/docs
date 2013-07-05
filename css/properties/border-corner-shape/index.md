{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Editor’s Draft}}
{{API_Name}}
{{Summary_Section|Specifies different corner clipping effects, such as scoop (inner curves), bevel (straight cuts) or notch (cut-off rectangles). Works along with border-radius to specify the size of each corner effect.}}
{{CSS Property
|Initial value=curve
|Applies to=all elements, except table element when ‘border-collapse’ is ‘collapse’
|Inherited=No
|Media=visual
|Computed value=as specified
|Animatable=No
|CSS object model property=element.style.borderCornerShape
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=curve
|Description=Border radii define a convex curve at the corner (default behavior of border-radius).
}}{{CSS Property Value
|Data Type=bevel
|Description=Border radii define a diagonal slice at the corner.
}}{{CSS Property Value
|Data Type=scoop
|Description=Border radii define a concave curve at the corner (informally called "negative border-radius")
}}{{CSS Property Value
|Data Type=notch
|Description=Border radii define a concave rectangular notch at the corner.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=Create a diamond (rhombus) shape
|Code=border-corner-shape: bevel;
border-radius: 50%;
}}{{Single Example
|Language=CSS
|Description=Create a trapezoid
|Code=border-corner-shape: bevel;
border-radius: 25% / 100% 100% 0 0;
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=Backgrounds & Borders Level 4
|URL=http://dev.w3.org/csswg/css-backgrounds-4/#border-corner-shape
|Status=W3C Editor’s Draft
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=No
|Chrome_version=
|Chrome_prefixed_supported=No
|Chrome_prefixed_version=
|Firefox_supported=No
|Firefox_version=
|Firefox_prefixed_supported=No
|Firefox_prefixed_version=
|Internet_explorer_supported=No
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=No
|Opera_version=
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=No
|Safari_version=
|Safari_prefixed_supported=No
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=No
|Android_version=
|Android_prefixed_supported=No
|Android_prefixed_version=
|Blackberry_supported=No
|Blackberry_version=
|Blackberry_prefixed_supported=No
|Blackberry_prefixed_version=
|Chrome_mobile_supported=No
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=No
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=No
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=No
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=No
|IE_mobile_version=
|IE_mobile_prefixed_supported=No
|IE_mobile_prefixed_version=
|Opera_mobile_supported=No
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=No
|Opera_mobile_prefixed_version=
|Opera_mini_supported=No
|Opera_mini_version=
|Opera_mini_prefixed_supported=No
|Opera_mini_prefixed_version=
|Safari_mobile_supported=No
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=No
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Box Model
|External_links=* [http://leaverou.github.com/border-corner-shape Preview of border-corner-shape with SVG]
}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}