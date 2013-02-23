{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Defines the shape of the border of the bottom-right corner.}}
{{CSS Property
|Initial value=0
|Applies to=All elements
|Inherited=No
|Media=visual
|Computed value=two absolute <length> or percentages
|Animatable=Yes
|CSS object model property=object.style.borderBottomRightRadius
|Values={{CSS Property Value
|Data Type=length
|Description=Denotes the size of the circle radius or the semi-major and semi-minor axes of the ellipsis. It can be expressed in any unit allowed by the [[css/data_types/length|CSS <length> data types]]. Negative values are invalid.
}}{{CSS Property Value
|Data Type=percentage
|Description=Denotes the size of the circle radius, or the semi-major and semi-minor axes of the ellipsis, using percentage values. Percentages for the horizontal axis refer to the width of the box, percentages for the vertical axis refer to the height of the box. Negative values are invalid.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=One value example to use an arc of circle as the border on the top left corner.
|Code=border-bottom-right-radius: 10px;

/* is equivalent to: */
border-bottom-right-radius: 10px 10px;
|LiveURL=[https://developer.mozilla.org/en-US/docs/CSS/border-bottom-right-radius View MDN's example
}}{{Single Example
|Language=CSS
|Description=Two value example to use an arc of ellipse as the border on the top left corner.
|Code=border-bottom-right-radius: 10px 5px;
}}{{Single Example
|Language=CSS
|Description=One value percentage example on the top left corner. If the box is a square an arc of circle is used as the border, if the box is not a square an arc of ellipse is used as the border.
|Code=border-bottom-right-radius: 30%;
}}
}}
{{Notes_Section
|Notes====Remarks===
The '''border-bottom-right-radius''' property specifies the horizontal and vertical radii of the ellipse that defines the rounded lower-right corner of a border box. If there is only one value given, that value specifies both horizontal and vertical radii of the ellipse. If there are two values given, the first value sets the horizontal radius and the second value sets the vertical radius.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Backgrounds and Borders Module Level 3: Rounded Corners:
|URL=http://www.w3.org/TR/css3-background/#border-bottom-right-radius
|Status=Candidate Recommendation
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=4.0
|Chrome_prefixed_supported=Yes
|Chrome_prefixed_version=0.2
|Firefox_supported=Yes
|Firefox_version=4.0 (2.0)
|Firefox_prefixed_supported=Yes
|Firefox_prefixed_version=1.0 (1.0)
|Internet_explorer_supported=Yes
|Internet_explorer_version=9.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=10.5
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=5.0
|Safari_prefixed_supported=Yes
|Safari_prefixed_version=3.0
}}{{Compatibility Table Desktop Row
|Feature=Percentages
|Chrome_supported=Yes
|Chrome_version=4.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=4.0 (2.0)
|Firefox_prefixed_supported=Yes
|Firefox_prefixed_version=1.0 (1.0)
|Internet_explorer_supported=Yes
|Internet_explorer_version=9.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=10.5
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=5.0
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}{{Compatibility Table Desktop Row
|Feature=Elliptical corners
|Chrome_supported=Yes
|Chrome_version=0.2
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=3.5 (1.9.1)
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=9.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=10.5
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=3.0
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_version=2.2
|Android_prefixed_supported=Yes
|Android_prefixed_version=2.1
|Blackberry_supported=Yes
|Blackberry_version=7.0
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=18.0
|Chrome_mobile_prefixed_supported=No
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=15.0
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Yes
|IE_mobile_version=9.0
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_version=11.0
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=No
|Opera_mini_version=
|Opera_mini_prefixed_supported=No
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=4.0
|Safari_mobile_prefixed_supported=Yes
|Safari_mobile_prefixed_version=3.2
}}
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Version=9.0
|Note=The border-bottom-right-radius property can't be animated/transitioned in IE.
}}
}}
{{See_Also_Section
|Topic_clusters=Border
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>Reference</code>
*<code>[[css/properties/border-radius|border-radius]]</code>
*<code>[[css/properties/border-top-left-radius|border-top-left-radius]]</code>
*<code>[[css/properties/border-top-right-radius|border-top-right-radius]]</code>
*<code>[[css/properties/border-bottom-left-radius|border-bottom-left-radius]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=[https://developer.mozilla.org/es/docs/CSS/border-bottom-right-radius Border-bottom-right-radius]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}